---
title: "`expandEntityReferences` が `NodeIterator` と `TreeWalker` から削除されました"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
releases: ["21", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=672190"
      title: "Bug 672190 – consider removing expandEntityReferences from NodeIterator and TreeWalker"
---
実体参照ノードの子要素がオブジェクトに対して可視かどうかを示すフラグを返す [`expandEntityReferences`](https://developer.mozilla.org/docs/Web/API/NodeIterator.expandEntityReferences) プロパティが、まったく役に立っていないとして、[`NodeIterator`](https://developer.mozilla.org/docs/Web/API/NodeIterator)、[`TreeWalker`](https://developer.mozilla.org/docs/Web/API/TreeWalker) 両オブジェクトから削除されました。
