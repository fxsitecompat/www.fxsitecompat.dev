---
title: "`<a>` 要素をイメージマップ領域として使用できなくなりました"
date: "2017-11-09T09:12:00-05:00"
categories: ["html"]
tags: []
versions: ["58"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1317937"
      title: "Bug 1317937 - Stop supporting <a> as <area> in image maps (Assertion failure: !aContent->GetPrimaryFrame() || aState.mCreatingExtraFrames || aContent->NodeInfo()->NameAtom() == nsGkAtoms::area, at nsCSSFrameConstructor.cpp:5687)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/JUB5K-sz6ek/discussion"
      title: "Intent to unship: <a> as <area> in image maps"
---
HTML 4 では、[`<a>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/a) 要素を `coords` や `shape` 属性と組み合わせることで、[`<area>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/area) 要素のように [`<map>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/map) 上のホットスポット領域として使用することが可能でした。この機能は他のどのブラウザにも実装されておらず HTML 5 仕様からも削除されたため、Firefox 58 で対応が廃止されました。
