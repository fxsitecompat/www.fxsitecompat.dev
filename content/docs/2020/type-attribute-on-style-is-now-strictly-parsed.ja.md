---
title: "`<style>` の `type` 属性が厳密に解釈されるようになりました"
date: "2020-03-11T01:27:00-04:00"
categories: ["css", "html"]
tags: []
releases: ["75"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1614329"
      title: "Bug 1614329 - style element's type attribute isn't parsed per the HTML spec rules"
---
Firefox 75 以降、`<style>` 要素上の `type` 属性が HTML 仕様に従って厳密に解釈されます。他のブラウザーは既に仕様に従っているため、この変更が公開サイトへ影響を及ぼす可能性は低いと思われますが、もしあなたがこれまで Firefox だけでサイトをテストしていた場合、単純ミスがあっても見逃してしまっている可能性があります。

以下の `<style>` 要素は有効です:

```html
<style></style>
<style type=""></style>
<style type="text/css"></style>
<style type="TEXT/CSS"></style>
```

以下の `<style>` 要素は無効で、スタイルシートは無視されます:

```html
<style type=" text/css "></style>
<style type="text/css; charset=utf-8"></style>
```
