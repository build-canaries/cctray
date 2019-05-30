---
layout: page
title:  "Servers"
permalink: /servers/
---

List of servers (in alphabetical order) that provide a CCTray feed:

### Buildkite

* Server home: <https://buildkite.com/>
* Default feed location: `https://cc.buildkite.com/[org_slug].xml?access_token=[access_token]`
* CCMenu setup instructions: <https://buildkite.com/docs/integrations/cc-menu>

### Buddybuild

* Server home: <https://www.buddybuild.com/>
* CCMenu setup instructions: <http://docs.buddybuild.com/docs/ccmenu>

### CircleCI

* Server home: <https://circleci.com/>
* Default feed location: `/cc.xml?circle-token=[api_token]`
  * Generate your personal API token at <https://circleci.com/account/api>
* CCMenu autodetect feed URL: not supported
* Note: Only available for default branch of the projects you follow.

### CruiseControl.NET

* Server home: <https://ccnet.github.io/CruiseControl.NET/projects/ccnet/wiki.html>
* Default feed location: `/XmlStatusReport.aspx` or `/ccnet/XmlStatusReport.aspx`
* CCMenu autodetect feed URL: supported

### Go

* Server home: <http://www.go.cd/>
* Default feed location: `/go/cctray.xml`
* CCMenu autodetect feed URL: supported
  
### Jenkins

* Server home: <http://jenkins-ci.org/>
* Default feed location: `/cc.xml` or `/hudson/cc.xml`
* Jenkins version 2.173+ needs to install CCtray XML Plugin: https://plugins.jenkins.io/cctray-xml
* CCMenu autodetect feed URL: supported
* Note: If you have problems with authentication, please check that you have CCMenu 1.9 or newer.

### Nevercode

* Server home: <https://nevercode.io/>
* CCMenu setup instructions: <https://developer.nevercode.io/docs/ccmenu-buildnotify-cctray>

### Semaphore

* Server home: <https://semaphoreci.com/>
* CCMenu setup instructions: <https://github.com/renderedtext/semaphore-docs-new/blob/master/source/docs/cctry.md>

### TeamCity

* Server home: <https://www.jetbrains.com/teamcity/>
* Default feed location: `/httpAuth/app/rest/cctray/projects.xml`
* CCMenu setup instructions: <http://confluence.jetbrains.com/display/TW/REST+API#RESTAPI-CCTray/>

### Travis

* Server home: <https://travis-ci.org>
* Default feed location:  `https://api.travis-ci.org/repositories/{user}/{repo}/cc.xml`
* CCMenu autodetect feed URL: not supported
* CCMenu setup instructions: <http://docs.travis-ci.com/user/cc-menu/>

## Historic

### CruiseControl

* Server home: <http://cruisecontrol.sourceforge.net/>
* Default feed location (classic): `/xml`
* Default feed location (dashboard): `/cctray.xml` or `/dashboard/cctray.xml`
* CCMenu autodetect feed URL: supported

### CruiseControl.rb

* Server home: <https://github.com/thoughtworks/cruisecontrol.rb>
* Default feed location: `/XmlStatusReport.aspx` or `/ccnet/XmlStatusReport.aspx`
* CCMenu autodetect feed URL: supported

### Hudson

* Server home: <http://hudson-ci.org/>
* Default feed location: `/cc.xml` or `/hudson/cc.xml`
* CCMenu autodetect feed URL: supported
k