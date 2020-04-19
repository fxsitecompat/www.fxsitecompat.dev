---
title: "アプリマニフェスト内の URL は配信元の代わりにマニフェスト URL に対して解決されるようになりました"
date: "2014-09-01T22:12:15-04:00"
categories: ["dom"]
tags: []
releases: ["34", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1042881"
      title: "Bug 1042881 – Resolve manifest properties urls against the manifest url instead of the origin."
---
[Open Web App マニフェスト](https://developer.mozilla.org/Apps/Build/Manifest) の項目内で指定された URL が、そのアプリの配信元ではなく、マニフェストファイルの URL に対して解決されるようになりました。この変更は、[同一配信元](https://developer.mozilla.org/docs/Web/Security/Same-origin_policy) から複数のアプリをインストール可能にするための措置です。
