---
title: "`text-decoration:blink` による点滅効果が削除されました"
date: "2013-04-06T04:52:59-04:00"
categories: ["css"]
tags: []
versions: ["23"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=857820"
      title: "Bug 857820 – Drop only blink effect from text-decoration: blink; and completely remove <blink> element"
---
Firefox は従来、CSS [`text-decoration`](https://developer.mozilla.org/ja/docs/Web/CSS/text-decoration) プロパティの `blink` キーワードを用いた Netscape 由来の点滅効果に対応していました。HTML [`<blink>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/blink) 要素や DOM [`String.blink`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/blink) メソッドでも同様の効果が得られました。Firefox 23 以降、この点滅効果は動作しなくなります。CSS パーサと DOM API による `text-decoration:blink` への対応は継続されますが、HTML パーサから [`<blink>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/blink) 要素への対応が削除されたため、この要素は未知の要素として扱われるようになります。Internet Explorer、Chrome、Safari は点滅効果に対応していません。Opera もまた、Blink レンダリングエンジンへの移行により、対応を中止するものと思われます。
