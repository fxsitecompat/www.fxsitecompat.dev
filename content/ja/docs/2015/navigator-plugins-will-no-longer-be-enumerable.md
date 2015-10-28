---
title: "`navigator.plugins` が列挙不可能となります"
date: "2015-10-26T21:49:00-07:00"
categories: ["dom", "plugins", "privacy-security"]
tags: []
versions: ["future"]
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=757726": "Bug 757726 - disallow enumeration of navigator.plugins"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=934107": "Bug 934107 - [meta] Remove use of plugin enumeration"
---
[`navigator.plugins`](https://developer.mozilla.org/ja/docs/Web/API/NavigatorPlugins/plugins) プロパティによって返される値が、フィンガープリンティングを最小限に抑えるため、将来的に列挙不可能となります。この変更は元々 Firefox 28 で予定されていましたが、いくつものサイトが影響を受けるため延期されています。なお、Firefox は [2016 年末までに Flash を除きプラグイン対応を廃止する予定](https://www.fxsitecompat.com/ja/docs/2015/plug-in-support-will-be-dropped-by-the-end-of-2016-except-flash/) ですので、いずれにしてもあなたのサイトでプラグインコンテンツを提供するのを避けるべきでしょう。
