---
title: "Audio Data API has been disabled"
date: "2013-12-09T02:32:17-05:00"
categories: ["audio-video"]
tags: []
releases: ["28", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=927245"
      title: "Bug 927245 – Remove deprecated Audio Data API implementation"
---
The experimental, non-standard [Audio Data API](https://developer.mozilla.org/docs/Introducing_the_Audio_API_Extension), which has been [deprecated since Firefox 22](https://www.fxsitecompat.dev/en-CA/docs/2013/audio-data-api-has-been-deprecated/), is now disabled behind the preference `media.audio_data.enabled`. The API will be [removed from Firefox 31](https://www.fxsitecompat.dev/en-CA/docs/2014/audio-data-api-has-been-removed/). The standardized [Web Audio API](https://developer.mozilla.org/docs/Web_Audio_API) can be used instead.
