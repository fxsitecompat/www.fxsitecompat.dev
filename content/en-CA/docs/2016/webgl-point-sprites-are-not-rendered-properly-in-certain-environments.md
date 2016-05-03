---
title: "WebGL point sprites are not rendered properly in certain environments"
date: "2016-04-29T05:20:00-04:00"
categories: ["canvas-webgl"]
tags: []
versions: ["46"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1268096"
      title: "Bug 1268096 - WebGL point sprites malfunctions in Firefox 46 on Windows D3D11 ANGLE"
---
Firefox 46 has introduced a regression in WebGL where point sprites, particle effects in particular, are broken on Windows 7 and Windows Server 2008 R2 due to an older, regressed version of the ANGLE library. This issue will be solved by porting ANGLE's upstream fix.

**Update**: This bug has been fixed with Firefox 47 Beta.
