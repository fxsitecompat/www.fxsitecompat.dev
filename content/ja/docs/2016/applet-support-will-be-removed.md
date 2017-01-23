---
title: "`<applet>` 対応が廃止されます"
date: "2016-10-05T18:38:00-04:00"
categories: ["dom", "html", "plugins"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1279218"
      title: "Bug 1279218 - Remove <applet> element"
---
法人ユーザー向けの ESR チャンネルを除く Firefox 52 で [Java プラグインへの対応が削除](https://www.fxsitecompat.com/ja/docs/2016/plug-in-support-has-been-dropped-other-than-flash/) された後、廃止予定となっている `HTMLAppletElement` インターフェイスへの対応が削除されます。[`<applet>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/applet) 要素は [`HTMLUnknownElement`](https://developer.mozilla.org/ja/docs/Web/API/HTMLUnknownElement) となります。[`document.applets`](https://developer.mozilla.org/ja/docs/Web/API/Document/applets) プロパティは後方互換性のため残されますが、常に空のコレクションを返すようになります。
