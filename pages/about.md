---
layout: page
title:  "About"
permalink: /about/
---

## Introduction

Various Continuous Integration monitoring/reporting tools exist. These tools work by polling Continuous Integration 
servers for summary information and presenting it appropriately to users.

If a Continuous Integration server can offer a standard summary format, and a reporting tool can consume the same, then 
we get interoperability between reporting tools and CI Servers.

Over the years the _CCTray_ format has become the de-facto standard for this purpose. Many CI servers implement their 
own, richer, APIs but also implement the _CCTray_ feed to support various monitoring tools.

## Links

[The current spec](/v1) provides technical information about the _CCTray_ format.

[The servers page](/servers) lists known servers and whether they support the _CCTray_ format.

[The clients page](/clients) lists known clients that can read the _CCTray_ format.

## Helping out

If you notice missing, inaccurate or out of date information, please [submit a pull request on GitHub](https://github.com/build-canaries/cctray)
to get the information updated.
