---
layout: page
title:  "CCTray v1"
date:   2005-10-07 10:23:00 +0000
updated: 2019-03-06 10:00:00 +0000
permalink: /v1/
---

## Introduction

Various Continuous Integration monitoring/reporting tools exist. These tools work by polling Continuous Integration servers for summary information and presenting it appropriately to users.

If a Continuous Integration server can offer a standard summary format, and a reporting tool can consume the same, then we get interoperability between reporting tools and CI Servers.

Over the years the _CCTray_ format has become the de-facto standard for this purpose. Many CI servers implement their own, richer, APIs but also implement the _CCTray_ feed to support various monitoring tools, including CCMenu.

## Description

Summary information will be available as a plain XML string retrievable through an HTTP GET request.

A single `<Projects>` node, the document root, which contains 0 or many `<Project>` nodes.

Each `<Project>` may have the following attributes:

name|description|type|required
----|-----------|----|--------
name|the name of the project|string|yes
activity|the current state of the project|string enum : Sleeping, Building, CheckingModifications|yes
lastBuildStatus|a brief description of the last build|string enum : Success, Failure, Exception, Unknown|yes
lastBuildLabel|a referential name for the last build|string|no
lastBuildTime|when the last build occurred|DateTime|yes
nextBuildTime|when the next build is scheduled to occur (or when the next check to see whether a build should be performed is scheduled to occur)|DateTime|no
webUrl|a URL for where more detail can be found about this project|string (URL)|yes

Clients that consume this XML should not rely on any optional attribute being present and should degrade their functionality gracefully.

### Example
{% highlight xml %}
<Projects>
    <Project
        name="SvnTest"
        activity="Sleeping"
        lastBuildStatus="Exception"
        lastBuildLabel="8"
        lastBuildTime="2005-09-28T10:30:34.6362160+01:00"
        nextBuildTime="2005-10-04T14:31:52.4509248+01:00"
        webUrl="http://mrtickle/ccnet/"/>

    <Project
        name="HelloWorld"
        activity="Sleeping"
        lastBuildStatus="Success"
        lastBuildLabel="13"
        lastBuildTime="2005-09-15T17:33:07.6447696+01:00"
        nextBuildTime="2005-10-04T14:31:51.7799600+01:00"
        webUrl="http://mrtickle/ccnet/"/>
</Projects>
{% endhighlight %}

<h3 id="specification">Schema</h3>

[Download](/schema/cctray-1.0.0.xsd)

{% highlight xml %}
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema" elementFormDefault="qualified">
  <xs:element name="Projects">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="Project" maxOccurs="unbounded">
          <xs:complexType>
            <xs:attribute name="name" type="xs:NMTOKEN" use="required" />
            <xs:attribute name="activity" use="required">
              <xs:simpleType>
                <xs:restriction base="xs:NMTOKEN">
                  <xs:enumeration value="Sleeping" />
                  <xs:enumeration value="Building" />
                  <xs:enumeration value="CheckingModifications" />
                </xs:restriction>
              </xs:simpleType>
            </xs:attribute>
            <xs:attribute name="lastBuildStatus" use="required">
              <xs:simpleType>
                <xs:restriction base="xs:NMTOKEN">
                  <xs:enumeration value="Exception" />
                  <xs:enumeration value="Success" />
                  <xs:enumeration value="Failure" />
                  <xs:enumeration value="Unknown" />
                </xs:restriction>
              </xs:simpleType>
            </xs:attribute>
            <xs:attribute name="lastBuildLabel" type="xs:NMTOKEN" use="required" />
            <xs:attribute name="lastBuildTime" type="xs:dateTime" use="required" />
            <xs:attribute name="nextBuildTime" type="xs:dateTime" use="optional" />
            <xs:attribute name="webUrl" type="xs:string" use="required" />
          </xs:complexType>
        </xs:element>
      </xs:sequence>
    </xs:complexType>
  </xs:element>
</xs:schema>
{% endhighlight %}
