---
date: "2018-05-13T17:24:00-04:00"
title: "Developer Tools"
description: "We are creating a couple of tools to make developers’ life easier."
slug: "tools"
---
## Compatibility Dataset

Based on [our 700+ articles](https://www.fxsitecompat.com/en-CA/docs/), we will release a fresh, accurate site compatibility dataset that covers the status of the obsolete features on each Firefox channel including Nightly, Beta/DevEdition and ESR. The data will be available by Q3 2018 in the portable JSON format.

Obviously, we are not aiming at creating comprehensive browser support tables that can be seen on *MDN*, *Can I use* or *QuirksMode*, but with the per-channel deprecation details, we hope both Firefox developers and web developers will find our own dataset useful.

## Compatibility Checker

With the fundamental data in hand, we will offer a [Firefox Developer Tools](https://developer.mozilla.org/docs/Tools) extension as well that shows a list of any removed or deprecated features used on the current page, so web developers can fix them right away. Due to technical limitations, it's not possible to check all the features covered in our upcoming dataset, but most issues in [HTML](https://www.fxsitecompat.com/en-CA/categories/html/), [CSS](https://www.fxsitecompat.com/en-CA/categories/css/), [JavaScript](https://www.fxsitecompat.com/en-CA/categories/javascript/) and [DOM](https://www.fxsitecompat.com/en-CA/categories/dom/) should be able to be flagged.

An extension for Visual Studio Code is also planned.

The checker may utilize part of external compatibility data to deal with unsupported features as well as other browsers, and also enhance the functionality with some utilities like regression alerts and reporter.
