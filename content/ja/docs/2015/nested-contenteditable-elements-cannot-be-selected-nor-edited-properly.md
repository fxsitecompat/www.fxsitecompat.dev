---
title: "入れ子になった `contenteditable` 要素が正常に選択、編集できません "
date: "2015-07-07T13:46:34-04:00"
categories: ["html"]
tags: ["regression"]
versions: "39"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1181130": "Bug 1181130 - Broken selection system inside of a nested contenteditable element"
---
Firefox 39 で、入れ子になった [内容の編集が可能な](https://developer.mozilla.org/ja/docs/Web/HTML/Content_Editable) 要素上でのテキスト選択や編集に関するリグレッションが発生したと、[CKEditor](http://ckeditor.com/) の開発者から報告がありました。キャレットがクリックされた場所に現れない、キャレットがキーボードのキー操作で動かない、編集不能要素もクリック時に選択されてしまうといった問題が発生しており、そのような要素上での編集が今のところ難しくなっています。Mozilla の開発者はこの問題を認識しており、解決策に取り組んでいます。

**更新**: バグに寄せられたコメントによれば、[MediaWiki VisualEditor](https://www.mediawiki.org/wiki/VisualEditor) の表編集機能も影響を受けています。このバグは Firefox 40 Beta と Firefox 41 Developer Edition では既に修正されています。
