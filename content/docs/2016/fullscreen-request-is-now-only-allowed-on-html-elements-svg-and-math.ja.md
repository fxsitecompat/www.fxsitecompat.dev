---
title: "全画面表示リクエストが HTML 要素、`<svg>`、`<math>` のみに許可されるようになりました"
date: "2016-10-16T03:06:00-04:00"
categories: ["dom"]
tags: []
releases: ["52", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1305928"
      title: "Bug 1305928 - Fullscreen request should only be allowed for HTML element, <svg>, and <math>"
---
Firefox 52 以降、最新の Fullscreen API 仕様に従い、HTML 要素と [`<svg>`](https://developer.mozilla.org/docs/Web/SVG/Element/svg)、[`<math>`](https://developer.mozilla.org/docs/Web/MathML/Element/math) 以外の要素に [`Element.requestFullscreen`](https://developer.mozilla.org/docs/Web/API/Element/requestFullscreen) メソッドを使用できなくなりました。なお、このメソッドは Firefox Beta、Release 両チャンネルでは [まだ接頭辞付き](https://www.fxsitecompat.dev/ja/docs/2016/fullscreen-api-has-been-unprefixed-in-non-release-builds/) となっています。
