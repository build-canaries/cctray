---
layout: page
title:  "Servers"
updated: 2022-11-30 20:47:00 +0000
permalink: /servers/
---

## Supported

List of servers (in alphabetical order) that provide a CCTray feed.

__Disclaimer__, third party plugins are provided for informational purposes only, and should not be taken as recommendations.

### [AWS CodeBuild](https://docs.aws.amazon.com/codebuild/index.html)

* Not natively supported
* Third party plugins 
  * [aws-codepipeline-ccxml](https://github.com/subnova/aws-codepipeline-ccxml/tree/master)
  * [CCStar](https://github.com/symphoniacloud/ccstar)

### [Bamboo](https://www.atlassian.com/software/bamboo)

* Not natively supported
* Third party plugins
  * [Bamboo CCTray proxy](https://github.com/chadlwilson/bamboo_cctray_proxy)

### [Buildkite](https://buildkite.com/)

* Default feed location `https://cc.buildkite.com/{org_slug}.xml?access_token={access_token}`
* [Buildkite CCTray documentation](https://buildkite.com/docs/integrations/cc-menu)

### [CircleCI](https://circleci.com/)

* Feed locations 
  * `https://circleci.com/cc.xml?circle-token={api_token}` default branches of the projects you follow
  * `https://circleci.com/gh/{organization}/{project}/tree/{branch}.cc.xml?circle-token={api_token}` specific branch of the project
  * Generate your personal API token at <https://circleci.com/account/api>

### [Cirrus CI](https://cirrus-ci.com)

* Default feed location `https://api.cirrus-ci.com/github/{user}/{repo}/cctray.xml`
* [Cirrus CI CCTray documentation](https://cirrus-ci.org/guide/writing-tasks/#cctray-xml)

### [Concourse](https://concourse-ci.org/)

* Default feed location `/api/v1/teams/{team}/cc.xml`
* [Concourse CCTray documentation](https://concourse-ci.org/observation.html#ccxml)

### [Drone CI](https://drone.io/)

* Default feed location `/api/badges/{owner}/{name}/cc.xml`

### [GitHub Actions](https://github.com/features/actions)

* Not natively supported
* Third party plugins
  * [CCTray Hub](https://github.com/idealo/cctray-hub/)

### [Gitlab CI](https://about.gitlab.com/product/continuous-integration/) 

* Not natively supported
  * [Issue to add support to GitLab CI](https://gitlab.com/gitlab-org/gitlab/-/issues/16958)
* Third party plugins
  * [GitLab panorama](https://github.com/joblift/gitlab-panorama)

### [GoCD](https://www.gocd.org/)

* Default feed location `/go/cctray.xml`
  
### [Jenkins](https://www.jenkins.io/)

* Supported via [official CCTray XML Plugin](https://plugins.jenkins.io/cctray-xml)
  * Note: versions prior to 2.173 had native support
* Default feed location `/cc.xml`

### [Semaphore](https://semaphoreci.com/)

* Default feed location `/api/v1/projects/{hash_id}/cc.xml?auth_token={auth_token}&ccmenu=cc.xml`
* [Semaphore CCTray documentation](https://github.com/renderedtext/semaphore-docs-new/blob/master/source/docs/cctry.md)

### [TeamCity](https://www.jetbrains.com/teamcity/)

* Default feed location `/httpAuth/app/rest/cctray/projects.xml`
* [TeamCity CCTray documentation](https://confluence.jetbrains.com/display/TW/REST+API#RESTAPI-CCTray)

### [Travis CI](https://www.travis-ci.com/)

* Default feed location `https://api.travis-ci.org/repositories/{user}/{repo}/cc.xml`
* [Travis CI CCTray documentation](https://docs.travis-ci.com/user/cc-menu/)

## Unsupported

List of servers (in alphabetical order) that currently have no or unknown support for a CCTray feed.

* [Abstruse CI](https://github.com/bleenco/abstruse)
* [Agola](https://agola.io/)
* [Appcircle](https://appcircle.io/)
* [App Center](https://appcenter.ms/)
* [AppVeyor](https://www.appveyor.com/)
  * [Issue to add support to AppVeyor](https://github.com/appveyor/ci/issues/67)
* [Azure DevOps](https://azure.microsoft.com/en-us/products/devops/?nav=min)
* [Bitrise](https://bitrise.io/)
* [Buddy](https://buddy.works/)
* [Buildbot](https://buildbot.net/)
* [Codefresh](https://codefresh.io/)
* [Codemagic](https://codemagic.io/start/)
* [Codeship](https://codeship.com/)
* [Evergreen](https://github.com/evergreen-ci/evergreen)
* [Kraken CI](https://kraken.ci/)
* [Razorops](https://razorops.com/)
* [Vela](https://go-vela.github.io/docs/)
* [Vexor](https://vexor.io/)
* [Xcode Cloud](https://developer.apple.com/xcode-cloud/get-started/)

## Historic

List of servers (in alphabetical order) that have been discontinued.

* [Buddybuild](https://www.buddybuild.com/)
* [CruiseControl](http://cruisecontrol.sourceforge.net/)
* [CruiseControl.NET](https://ccnet.github.io/CruiseControl.NET/projects/ccnet/wiki.html)
* [CruiseControl.rb](https://github.com/thoughtworks/cruisecontrol.rb)
* [Hudson CI](https://github.com/hudson)
* [Solano CI](https://github.com/solanolabs)
* [Wercker](https://en.wikipedia.org/wiki/Wercker)
