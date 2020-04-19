---
title: "`DOMQuad.bounds` が `getBounds()` に置き換えられる形で廃止されました"
date: "2019-06-29T22:49:00-04:00"
categories: ["dom"]
tags: []
releases: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1454622"
      title: "Bug 1454622 - Change DOMQuad bounds to getBounds() as per specification"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/q01sJZp3LH8/discussion"
      title: "Intent to unship: DOMQuad.prototype.bounds"
---
現行の Geometry Interfaces 仕様に従って [Firefox 62](https://www.fxsitecompat.dev/ja/docs/2018/dompoint-constructor-no-longer-accepts-dompointinit-as-argument-domquad-bounds-has-been-deprecated/) 以降廃止予定となっていた [`DOMQuad`](https://developer.mozilla.org/docs/Web/API/DOMQuad) インターフェイス上の `bounds` プロパティが Firefox 69 で削除されました。他のどのブラウザーもこのプロパティに対応していないことから、互換性リスクは低いはずです。標準の `getBounds` メソッドで代用してください。
