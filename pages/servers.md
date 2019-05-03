---
layout: page
title:  "Servers"
permalink: /servers/
---

List of servers (in alphabetical order) that provide a CCTray feed:

### Buddybuild

* Server home: <https://www.buddybuild.com/>
* CCMenu setup instructions: <http://docs.buddybuild.com/docs/ccmenu>

### CircleCI

* Server home: <https://circleci.com/>
* Default feed location: `/cc.xml?circle-token=[api_token]`
  * Generate your personal API token at <https://circleci.com/account/api>
* CCMenu autodetect feed URL: not supported
* Note: Only available for default branch of the projects you follow.

### CruiseControl

* Server home: <http://cruisecontrol.sourceforge.net/>
* Default feed location (classic): `/xml`
* Default feed location (dashboard): `/cctray.xml` or `/dashboard/cctray.xml`
* CCMenu autodetect feed URL: supported

### CruiseControl.NET

* Server home: <https://ccnet.github.io/CruiseControl.NET/projects/ccnet/wiki.html>
* Default feed location: `/XmlStatusReport.aspx` or `/ccnet/XmlStatusReport.aspx`
* CCMenu autodetect feed URL: supported

### CruiseControl.rb

* Server home: <https://github.com/thoughtworks/cruisecontrol.rb>
* Default feed location: `/XmlStatusReport.aspx` or `/ccnet/XmlStatusReport.aspx`
* CCMenu autodetect feed URL: supported

### Go

* Server home: <http://www.go.cd/>
* Default feed location: `/go/cctray.xml`
* CCMenu autodetect feed URL: supported

### GreenhouseCI

* Server home: <http://greenhouseci.com/>
* CCMenu setup instructions: <http://blog.greenhouseci.com/greenhouse/update/ccmenu-support/>

### Hudson

* Server home: <http://hudson-ci.org/>
* Default feed location: `/cc.xml` or `/hudson/cc.xml`
* CCMenu autodetect feed URL: supported

### Jenkins

* Server home: <http://jenkins-ci.org/>
* Default feed location: `/cc.xml` or `/hudson/cc.xml`
* CCMenu autodetect feed URL: supported
* Note: If you have problems with authentication, please check that you have CCMenu 1.9 or newer.

### Semaphore

* Server home: <https://semaphoreapp.com/>
* CCMenu setup instructions: <https://github.com/renderedtext/semaphore-docs-new/blob/master/source/docs/cctry.md>

### TeamCity

* Server home: <https://www.jetbrains.com/teamcity/>
* CCMenu setup instructions: <http://confluence.jetbrains.com/display/TW/REST+API#RESTAPI-CCTray/>

### Travis

* Server home: <https://travis-ci.org>
* Default feed location:  `https://api.travis-ci.org/repositories/{user}/{repo}/cc.xml`
* CCMenu autodetect feed URL: not supported
* CCMenu setup instructions: <http://docs.travis-ci.com/user/cc-menu/>
