---
title: "`pt=` and `rid=` in WebRTC simulcast attributes are no longer supported"
date: "2019-10-09T23:17:00-04:00"
categories: ["audio-video"]
tags: []
releases: ["72"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1225877"
      title: "Bug 1225877 - Parse latest a=simulcast and a=rid"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1470568"
      title: "Bug 1470568 - Stop supporting \"rid=\" in simulcast attributes once ESR doesn't serialize it anymore"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1586423"
      title: "Bug 1586423 - meet.google.com / Google Hangouts doesn't work in Nightly (\"Couldn't start the video call because of an error\")"
---
Firefox 71 has stopped parsing the legacy `pt=` and `rid=` parameters in WebRTC simulcast attributes. The new format supported since Firefox 68 only requires a RID, so, for example,

```
a=simulcast: send rid=8 recv rid=9
```

has to be

```
a=simulcast: send 8 recv 9
```

Currently, video calls in *Google Hangouts Meet* and *Whereby* are broken due to this change.

**Update**: This change has been reverted in Firefox 71 to give services more time to adopt the new behaviour. Mozilla developers are planning to redo the change with Firefox 72.

**Update 2**: The change has been landed again to Firefox 72 after both *Google* and *Whereby* fixed their issue. If you run a similar service, please be sure to test it.
