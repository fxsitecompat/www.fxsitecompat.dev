---
title: "`NamedNodeMap` が `MozNamedAttrMap` へ改名されました"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
versions: ["22"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=847195"
      title: "Bug 847195 – Make NamedNodeMap only deal with Attrs"
---
[`NamedNodeMap`](https://developer.mozilla.org/docs/Web/API/NamedNodeMap) インターフェイスは、仕様から削除されたことと [`Node.attributes`](https://developer.mozilla.org/docs/Web/API/Node.attributes) でしか使用できないことから、接頭辞付きの `MozNamedAttrMap` へ改名されました。
