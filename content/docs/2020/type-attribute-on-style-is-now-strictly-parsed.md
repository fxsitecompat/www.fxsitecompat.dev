---
title: "`type` attribute on `<style>` is now strictly parsed"
date: "2020-03-11T01:27:00-04:00"
categories: ["css", "html"]
tags: []
releases: ["75"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1614329"
      title: "Bug 1614329 - style element's type attribute isn't parsed per the HTML spec rules"
---
Starting with Firefox 75, the `type` attribute on the `<style>` element will be strictly parsed as per the HTML spec. This change unlikely affects production sites since other browsers are already following the spec, but any simple mistake could have been missed if you have previously tested your site only with Firefox.

The following `<style>` elements are valid:

```html
<style></style>
<style type=""></style>
<style type="text/css"></style>
<style type="TEXT/CSS"></style>
```

The following `<style>` elements are invalid, so the stylesheets will be ignored:

```html
<style type=" text/css "></style>
<style type="text/css; charset=utf-8"></style>
```
