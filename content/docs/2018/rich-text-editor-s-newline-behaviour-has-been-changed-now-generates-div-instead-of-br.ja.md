---
title: "リッチテキストエディターの改行時の挙動が変更され、`<br>` の代わりに `<div>` が生成されます"
date: "2018-02-16T10:30:00-05:00"
categories: ["dom", "html"]
tags: []
versions: ["60", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1297414"
      title: "Bug 1297414 - Generate <p>/<div> for newlines, not <br> (defaultParagraphSeparator)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1430551"
      title: "Bug 1430551 - Make defaultPargraphSeparater <div> in release build"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/V7LMopGp5HY/discussion"
      title: "Intent to change editor newline behavior"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/X2bhfUG49RE/discussion"
      title: "Intent to enable <div> as default paragraph separator of contenteditable/designMode editor by default"
aliases:
    - "/ja/docs/2017/rich-text-editor-s-newline-behaviour-has-been-changed-now-generates-div-instead-of-br/"
---
Firefox では、[リッチテキストエディター](https://developer.mozilla.org/docs/Rich-Text_Editing_in_Mozilla) 上で Enter キーを押すと `<br>` 要素が挿入されます。一方、Internet Explorer では `<p>` が、Google Chrome では `<div>` が、それぞれ追加されます。多くの議論が重ねられた結果、Firefox 60 でこの挙動が Chrome に合わせる形で変更され、`<div>` が新たな既定のセパレーターとして使用されます。

「Firefox」と入力して「Fire」と「fox」の間で Enter を押すと、結果として得られる HTML は `Fire<br>fox` ではなく `<div>Fire</div><div>fox</div>` となります。

この挙動は、バージョン 55 以降の Firefox Nightly と早期 Beta/DevEdition では既に初期設定で有効となっていますが、[`execCommand`](https://developer.mozilla.org/docs/Web/API/Document/execCommand) メソッドの [`DefaultParagraphSeparator`](https://msdn.microsoft.com/en-us/library/hh801229(v=vs.85).aspx#DefaultParagraphSeparator) コマンドで制御可能です。

```js
// 従来通り <br> を挿入するには
document.execCommand("DefaultParagraphSeparator", false, "br");
// 代わりに <p> を生成するには
document.execCommand("DefaultParagraphSeparator", false, "p");
```
