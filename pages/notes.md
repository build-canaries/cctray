---
layout: page
title:  "Notes"
permalink: /notes/
---


# For server implementors

If you are implementing a CI server, please consider providing build information in the _cctray_ format, described on this site. This will make your server compatible with [CCMenu](http://ccmenu.org), [Nevergreen](https://github.com/build-canaries/nevergreen), and other tools that read the feed format.

The specification leaves some open questions. If in doubt, please:
* Provide times with a timezone, ideally in ISO8601 format with Zulu/GMT time marker.
* Use `unknown` status for all status values not mentioned in the standard.
* If you support authentication, please respond with `401 Not Authorized` and a `WWW-Authenticate` header to feed requests without authorization headers. Do not require cookies, and do not redirect to HTML forms.

If you would like your server to be mentioned on the [Supported Servers](/servers) page, please open a pull request with the relevant details. If you are offering a cloud hosted (SaaS) server you should include a link to setup instructions for CCMenu and/or other tools.