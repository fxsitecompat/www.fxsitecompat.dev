---
title: "プラグインの MIME タイプが小文字表記になっています"
date: "2013-12-09T02:32:17-05:00"
categories: ["dom", "plugins"]
tags: []
versions: ["28"]
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=206659"
      title: "Bug 206659 - Plugin not found, because MIME type has upper-case letters"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=985859"
      title: "Bug 985859 - navigator.mimeTypes has lower-cased MIME types since Firefox 28 while preserving case on earlier versions"
---
Firefox 28 で、[`document.plugins`](https://developer.mozilla.org/ja/docs/Web/API/document.plugins)、[`window.navigator.plugins`](https://developer.mozilla.org/ja/docs/Web/API/window.navigator.plugins)、[`window.navigator.mimeTypes`](https://developer.mozilla.org/ja/docs/Web/API/window.navigator.mimeTypes) の各プロパティで公開される MIME タイプが、元々の大小文字混在あるいは大文字から小文字表記に変わっています。これはリグレッションと見なされ、Firefox 29 で修正されました。回避策: 特定の MIME タイプを見つけようとする場合は [`String.toLowerCase`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/toLowerCase) メソッドを使ってください。
