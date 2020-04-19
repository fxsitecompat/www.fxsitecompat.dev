---
title: "`select.size` に負の値を指定した場合の挙動が変わります"
date: "2012-10-09T06:00:00-04:00"
categories: ["dom"]
tags: []
releases: ["16"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=760848"
      title: "Bug 760848 – select.size reflection is wrong"
---
[`<select>`](https://developer.mozilla.org/docs/Web/HTML/Element/select) 要素の `size` プロパティに負の値を与えた場合、従来は例外が投げられていましたが、今後は `0` と見なされます。
