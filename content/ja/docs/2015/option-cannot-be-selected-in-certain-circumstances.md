---
title: "特定の状況で `<option>` が選択できません"
date: "2015-08-16T03:45:05-04:00"
categories: ["html"]
tags: []
versions: "40"
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1194733": "Bug 1194733 - [Not e10s] Version 40.0.2 has issue with jquery ibutton plugin"
---
[`<select>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/select) 要素かその先祖要素上の [`mouseup`](https://developer.mozilla.org/ja/docs/Web/Reference/Events/mouseup) イベントハンドラ内で [`Event.preventDefault`](https://developer.mozilla.org/ja/docs/Web/API/Event/preventDefault) が呼び出された場合に、[`<option>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/option) 要素が選択できず、その親の `<select>` 要素も閉じることができません。[*iButton jQuery プラグイン*](http://www.givainc.com/labs/ibutton_jquery_plugin.cfm) が影響を受けることが判明しています。Mozilla 開発者が原因を把握し、解決策に取り組んでいます。

**更新**: この問題は <time datetime="2015-08-27">8 月 27 日</time> 公開の Firefox 40.0.3 で修正されました。
