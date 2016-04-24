---
title: "Disabled form controls now trigger `mouseover` and similar mouse events"
date: "2016-04-23T23:51:00-04:00"
categories: ["dom"]
tags: []
versions: ["44"]
statuses: "affected"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=218093"
      title: "Bug 218093 - disabled child element doesn't produce mouseout/mouseover pair"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1265909"
      title: "Bug 1265909 - FireFox 45.0.2 fires onMouseOut for disabled input."
---
Starting with Firefox 44, the [`mouseover`](https://developer.mozilla.org/en-US/docs/Web/Events/mouseover), [`mouseout`](https://developer.mozilla.org/en-US/docs/Web/Events/mouseout), [`mouseenter`](https://developer.mozilla.org/en-US/docs/Web/Events/mouseenter) and [`mouseleave`](https://developer.mozilla.org/en-US/docs/Web/Events/mouseleave) events will be fired for disabled form controls such as [`<input>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input). The old behaviour had sometimes confused Web developers using jQuery in particular.

In order to make sure your code always works as expected, you might want to explicitly check the `disabled` property of the target element in your event handler.
