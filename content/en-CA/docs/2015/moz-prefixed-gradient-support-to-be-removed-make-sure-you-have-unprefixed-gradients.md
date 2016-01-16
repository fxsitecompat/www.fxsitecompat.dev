---
title: "`-moz`-prefixed gradient support to be removed, make sure you have unprefixed gradients"
date: "2015-08-05T00:48:18-04:00"
categories: ["css"]
tags: []
versions: ["future"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1176496": "Bug 1176496 - Drop support for -moz-prefixed gradients (-moz-linear-gradient, -moz-radial-gradient)"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1186636": "Bug 1186636 - Add pref to control legacy -moz-prefixed gradients"
---
The `-moz-linear-gradient`, `-moz-repeating-linear-gradient`, `-moz-radial-gradient` and `-moz-repeating-radial-gradient` functions are to be gone in favour of the standard, unprefixed version of [CSS gradients](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Using_CSS_gradients) available since [Firefox 16](https://developer.mozilla.org/en-US/Firefox/Releases/16). Mozilla developers once removed the prefix support from the Firefox 42 Nightly builds, however, the change was backed out in a week due to a lot of broken sites where only legacy prefixed gradients are used in their stylesheets.

In order to help Web developers test sites with prefixed gradients disabled, a hidden preference has been added to Firefox 42. Here's how: open the preference editor by typing `about:config` in the location bar, search `layout.css.prefixes.gradients`, double-click on the preference item to flip the value, then load your site to make sure every part is displayed properly. If something is broken, unprefixed gradients, [`linear-gradient()`](https://developer.mozilla.org/en-US/docs/Web/CSS/linear-gradient), [`repeating-linear-gradient()`](https://developer.mozilla.org/en-US/docs/Web/CSS/repeating-linear-gradient), [`radial-gradient()`](https://developer.mozilla.org/en-US/docs/Web/CSS/radial-gradient) or [`repeating-radial-gradient()`](https://developer.mozilla.org/en-US/docs/Web/CSS/repeating-radial-gradient), are missing in your stylesheet.

Given the considerable number of broken sites, it may be difficult for Firefox to remove the legacy prefix support sometime soon, but developers should always be using unprefixed gradients to make your site future-proof. The same applies to any other CSS properties, values and functions, of course.
