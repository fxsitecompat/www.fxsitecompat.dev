---
title: "Scoped stylesheets are no longer supported"
date: "2017-07-13T22:33:00-04:00"
categories: ["css", "html"]
tags: []
releases: ["55", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1291515"
      title: "Bug 1291515 - disable <style scoped> in content documents"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/iBoROFkR9V8/discussion"
      title: "Intent to unship: HTML scoped style sheets (<style scoped>)"
supported_tools:
  firefox_extension: true
---
The support for [HTML scoped stylesheets](https://developers.google.com/web/updates/2012/03/A-New-Experimental-Feature-style-scoped), implemented with Firefox 21, is no longer available in web content because it has been removed from the HTML spec. This includes the [`scoped`](https://developer.mozilla.org/docs/Web/HTML/Element/style#attr-scoped) boolean attribute on the `<style>` HTML element, the [`scoped`](https://developer.mozilla.org/docs/Web/API/HTMLStyleElement/scoped) DOM property as well as the [`:scope`](https://developer.mozilla.org/docs/Web/CSS/:scope) CSS pseudo-class. Google Chrome has already [removed the implementation](https://www.chromestatus.com/feature/5374137958662144) and no other browsers support the feature at this time.
