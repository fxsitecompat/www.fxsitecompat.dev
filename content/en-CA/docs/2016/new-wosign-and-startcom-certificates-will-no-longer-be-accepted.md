---
title: "New WoSign and StartCom certificates will no longer be accepted"
date: "2016-10-25T09:17:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1309707"
      title: "Bug 1309707 - Distrust new certs chaining up to current WoSign/StartCom roots"
    - url: "https://blog.mozilla.org/security/2016/10/24/distrusting-new-wosign-and-startcom-certificates/"
      title: "Mozilla Security Blog: Distrusting New WoSign and StartCom Certificates"
---
Mozilla has discovered various "technical and management failures" of certificate authorities (CA) called WoSign and StartCom based on a careful investigation, and decided to distrust their new certificates issued after October 21, 2016. Their older certificates remain accepted to avoid the impact on the existing customers, however, the affected root certificates will be removed from Firefox in the future. See [this Security Blog post](https://blog.mozilla.org/security/2016/10/24/distrusting-new-wosign-and-startcom-certificates/) for details of the incident and Mozilla's action.
