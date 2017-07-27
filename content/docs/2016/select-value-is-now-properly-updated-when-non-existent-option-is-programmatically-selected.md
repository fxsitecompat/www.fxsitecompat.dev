---
title: "`<select>` value is now properly updated when non-existent option is programmatically selected"
date: "2016-04-24T08:25:00-04:00"
categories: ["dom"]
tags: []
versions: ["46"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1203668"
      title: "Bug 1203668 - changing the value of a select to a value that matches none of the options should put it in a \"no option selected\" state even when it's a combobox (size=1)"
---
Previously, using JavaScript to change the `value` property of a [`<select>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select) element to a value that matched no [`<option>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/option) did not update the selection accordingly, when the `<select>` element was displayed as a combobox.

Firefox 46 has fixed this bug as per the HTML spec so that any `<option>` will be unselected in such cases. That means the `selectedIndex`, `selectedOptions` and `value` properties of the `<select>` element will become `-1`, an empty `HTMLCollection` and an empty string respectively.

While the new behaviour should match other browsers, certain sites with Firefox-specific code could be broken with this change.
