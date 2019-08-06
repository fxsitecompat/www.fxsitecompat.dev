---
date: "2018-05-13T17:24:00-04:00"
title: "Developer Tools"
description: "We are creating a couple of tools to make developers’ life easier."
slug: "tools"
---
## Compatibility Dataset

Based on [our 800+ articles](https://www.fxsitecompat.dev/en-CA/docs/), we will release a fresh, accurate site compatibility dataset that covers the status of the obsolete features on each Firefox channel including Nightly, Beta/DevEdition and ESR. The data will be available in the portable JSON format.

Obviously, we are not aiming at creating comprehensive browser support tables that can be seen on *MDN*, *Can I use* or *QuirksMode*, but with the per-channel deprecation details, we hope both Firefox developers and web developers will find our own dataset useful.

## Firefox Extension

We are developing a [Firefox extension](https://addons.mozilla.org/firefox/addon/site-compatibility-tools/) as a handy all-in-one tool for web developers to learn, check and report site compatibility issues directly within Firefox Developer Tools. The initial release makes it easier to access our documents and report compatibility issues.

With the fundamental dataset in hand, we will integrate a compatibility checker into the extension that shows a list of any removed or deprecated features used on the current page, so web developers can fix them right away. Due to technical limitations, it's not possible to check all the features covered in our upcoming dataset, but most issues in [HTML](https://www.fxsitecompat.dev/en-CA/categories/html/), [SVG](https://www.fxsitecompat.dev/en-CA/categories/svg/), [CSS](https://www.fxsitecompat.dev/en-CA/categories/css/), [JavaScript](https://www.fxsitecompat.dev/en-CA/categories/javascript/) and [DOM](https://www.fxsitecompat.dev/en-CA/categories/dom/) should be able to be flagged.

<img src="/images/screenshots/firefox-extension-large.png" alt="" width="800" height="450">

## VS Code Extension

We also have a plan to release an extension for Visual Studio Code.
