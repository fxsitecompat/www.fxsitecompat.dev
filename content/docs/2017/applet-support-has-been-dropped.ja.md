---
title: "`<applet>` 対応が廃止されました"
date: "2017-07-13T21:19:00-04:00"
categories: ["dom", "html", "plugins"]
tags: []
versions: ["56"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1279218"
      title: "Bug 1279218 - Remove <applet> element"
aliases:
    - "/ja/docs/2016/applet-support-will-be-removed/"
---
廃止予定となっていた [`<applet>`](https://developer.mozilla.org/docs/Web/HTML/Element/applet) HTML 要素と `HTMLAppletElement` DOM インターフェイスへの対応が Firefox 56 で削除され、この要素は [`HTMLUnknownElement`](https://developer.mozilla.org/docs/Web/API/HTMLUnknownElement) となりました。Java プラグイン対応は、法人ユーザー向けの ESR チャンネルを除き、[Firefox 52](https://www.fxsitecompat.dev/ja/docs/2016/plug-in-support-has-been-dropped-other-than-flash/) で既に廃止されています。[`document.applets`](https://developer.mozilla.org/docs/Web/API/Document/applets) DOM プロパティは後方互換性のため残されますが、常に空のコレクションを返すようになります。
