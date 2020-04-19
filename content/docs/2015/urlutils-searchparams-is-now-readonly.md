---
title: "`URLUtils.searchParams` is now readonly"
date: "2015-06-13T15:20:46-04:00"
categories: ["dom"]
tags: []
versions: ["41", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1174731"
      title: "Bug 1174731 - Make searchParams attribute readonly"
---
The [`URLUtils.searchParams`](https://developer.mozilla.org/docs/Web/API/URLUtils/searchParams) property has been marked as readonly to reduce the complexity of the [`URLSearchParams`](https://developer.mozilla.org/docs/Web/API/URLSearchParams) interface. A workaround here is to stringify the parameters with [`URLSearchParams.toString`](https://developer.mozilla.org/docs/Web/API/URLSearchParams/toString) and assign the string with [`URLUtils.search`](https://developer.mozilla.org/docs/Web/API/URLUtils/search) ([example](https://github.com/bzdeck/bzdeck/commit/c0841f7f0bfe17fac71b606be6b3777049aea6dc)).
