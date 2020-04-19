---
title: "`DataTransfer.types` is now `DOMStringList` instead of `Array`"
date: "2016-12-16T02:13:00-05:00"
categories: ["dom"]
tags: []
versions: ["52", "52-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1298243"
      title: "Bug 1298243 - drag/drop: DataTransfer.types is wrong type"
---
Firefox was previously returning a [`DOMStringList`](https://developer.mozilla.org/docs/Web/API/DOMStringList) for the [`DataTransfer.prototype.types`](https://developer.mozilla.org/docs/Web/API/DataTransfer/types) property. Firefox 52 and above will return a simple `Array` of `DOMString`s in order to comply with the current HTML spec. That means the `contains` method no longer works on the property; the [`includes`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/includes) method should be used instead to check if a specific type of data is provided.

For the backward compatibility, you can use the [spread syntax](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Spread_operator) like this:

```js
document.body.addEventListener('drop', event => {
  event.preventDefault();

  if ([...event.dataTransfer.types].includes('text/html')) {
    // Do something
  }
});
```

**Update**: Drag and Drop of attachments in *JIRA* is broken due to this change. Atlassian has [fixed the issue](https://bitbucket.org/atlassian/jira-drag-drop-attachments-plugin/commits/3dbc08643607a680339d485877af501c0572e1b1); see [this thread](https://jira.atlassian.com/browse/JRA-64414) for the solution.
