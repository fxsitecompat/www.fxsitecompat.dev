---
title: "`Headers.getAll()` has been removed in favour of `get()` now returning all values"
date: "2016-11-16T15:51:00-05:00"
categories: ["dom"]
tags: []
versions: ["52", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1278275"
      title: "Bug 1278275 - Headers.get should incorporate getAll behaviour"
---
The [`Headers.prototype.getAll`](https://developer.mozilla.org/docs/Web/API/Headers/getAll) method has been removed as per the latest Fetch spec. Instead, the [`Headers.prototype.get`](https://developer.mozilla.org/docs/Web/API/Headers/get) method now returns the all values of a given HTTP header in a comma-separated string instead of just the first value.

```js
const headers = new Headers();
headers.append('Accept-Language', 'en');
headers.append('Accept-Language', 'fr');

// On Firefox 51 and prior
headers.get('Accept-Language'); // "en"
headers.getAll('Accept-Language'); // ["en", "fr"]

// On Firefox 52 and later
headers.get('Accept-Language'); // "en,fr"
```
