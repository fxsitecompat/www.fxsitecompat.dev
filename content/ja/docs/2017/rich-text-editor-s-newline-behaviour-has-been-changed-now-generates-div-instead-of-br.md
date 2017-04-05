---
title: "リッチテキストエディターの改行時の挙動が変更され、`<br>` の代わりに `<div>` が生成されます"
date: "2017-04-05T09:02:00-04:00"
categories: ["misc"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1297414"
      title: "Bug 1297414 - Generate <p>/<div> for newlines, not <br> (defaultParagraphSeparator)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/V7LMopGp5HY/discussion"
      title: "Intent to change editor newline behavior"
---
Firefox では、[リッチテキストエディター](https://developer.mozilla.org/ja/docs/Rich-Text_Editing_in_Mozilla) 上で Enter キーを押すと `<br>` 要素が挿入されます。一方、Internet Explorer では `<p>` が、Google Chrome では `<div>` が、それぞれ追加されます。多くの議論が重ねられた結果、Firefox 55 でこの挙動が Chrome に合わせる形で変更され、`<div>` が新たな既定のセパレーターとして使用されます。

「Firefox」と入力して「Fire」と「fox」の間で Enter を押すと、結果として得られる HTML は `Fire<br>fox` ではなく `<div>Fire</div><div>fox</div>` となります。

この挙動は [`execCommand`](https://developer.mozilla.org/ja/docs/Web/API/Document/execCommand) メソッドの [`DefaultParagraphSeparator`](https://msdn.microsoft.com/en-us/library/hh801229(v=vs.85).aspx#DefaultParagraphSeparator) コマンドで制御可能です。

```js
// 従来通り <br> を挿入するには
document.execCommand("DefaultParagraphSeparator", false, "br");
// 代わりに <p> を生成するには
document.execCommand("DefaultParagraphSeparator", false, "p");
```
