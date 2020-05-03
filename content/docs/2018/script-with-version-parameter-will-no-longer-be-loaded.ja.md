---
title: "バージョン引数の付いた `<script>` は読み込まれなくなりました"
date: "2018-02-23T19:19:00-05:00"
categories: ["html", "javascript"]
tags: []
releases: ["59", "60-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=867609"
      title: "Bug 867609 - Retire JavaScript versions"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=867612"
      title: "Bug 867612 - Make sure JavaScript version is not used on the web"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1428745"
      title: "Bug 1428745 - Remove support for version parameter from script loader"
aliases:
    - "/ja/docs/2015/javascript-versions-will-be-retired/"
supported_tools:
  firefox_extension: true
---
Firefox では伝統的に、JavaScript [1.7](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.7) や [1.8](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.8) の高度な機能を利用するには、`<script>` 要素の `type` 属性に `version` 引数を明示する必要がありました。

```html
<script type="application/javascript;version=1.7"></script>
<script type="application/javascript;version=1.8"></script>
```

Firefox 44 以降、`let` 命令文は [明示的な JavaScript バージョンを必要としなくなりました](https://www.fxsitecompat.dev/ja/docs/2015/let-statement-no-longer-requires-explicit-javascript-version/)。一方、JavaScript 1.7 と 1.8 で追加された [分割代入型 `for-in`](https://www.fxsitecompat.dev/ja/docs/2015/destructuring-for-in-loop-has-been-removed/)、[旧式イテレーター](https://www.fxsitecompat.dev/ja/docs/2017/legacy-iterator-protocol-has-been-removed/)、[旧式ジェネレーター](https://www.fxsitecompat.dev/ja/docs/2017/legacy-generator-support-has-been-removed/)、[配列内包](https://www.fxsitecompat.dev/ja/docs/2017/array-generator-comprehension-support-has-been-removed/)、[式クロージャー](https://www.fxsitecompat.dev/ja/docs/2017/expression-closure-support-has-been-removed/) への対応は、それぞれ標準の機能に取って代わられる形で廃止されました。

標準化活動の一環として、この Firefox 固有の JavaScript `version` 引数対応も Firefox 59 で廃止されました。つまり、何らかの `version` 引数が付いた `<script>` は、`text/template` のような未知の MIME タイプのスクリプトとして扱われるため、読み込まれなくなります。Mozilla の調査によれば、この変更は 0.02% のスクリプト読み込みに影響する可能性があります。

JavaScript を配信している場合、HTML5 やより新しい HTML Living Standard ではオプションとなっている `type` 属性を単純に省略することができますし、そうしない場合は `text/javascript` や `application/javascript` など [標準 JavaScript MIME タイプ](https://mimesniff.spec.whatwg.org/#javascript-mime-type) のいずれかを引数抜きで使用しなくてはなりません。
