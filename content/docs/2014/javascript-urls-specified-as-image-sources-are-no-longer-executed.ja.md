---
title: "画像ソースとして指定された `javascript` URL は実行されなくなります"
date: "2014-07-22T05:06:26-04:00"
categories: ["javascript"]
tags: []
versions: ["33"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1018583"
      title: "Bug 1018583 – <style>background: url(\'javascript:while(true){}\');</style> hangs Firefox"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/UsspiA5a3Ok/discussion"
      title: "Intent to unship: javascript: execution outside navigation contexts"
---
従来、[`<img>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/img) `src` や CSS 背景画像として指定された `javascript` URL は、通常の JavaScript コードとして解析、実行されていましたが、ブラウザーをハングさせるために悪用され、サービス妨害 (DoS) 攻撃につながることから、この手法は使用できなくなりました。
