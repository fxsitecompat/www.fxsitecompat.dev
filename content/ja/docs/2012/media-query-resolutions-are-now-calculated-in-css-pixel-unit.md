---
title: "メディアクエリの解像度が CSS ピクセル単位で計算されるようになりました"
date: "2012-10-09T06:00:00-04:00"
categories: ["css"]
tags: []
versions: ["16"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=771390"
      title: "Bug 771390 – [css3-mediaqueries] resolution units (dpi, dpcm, dppx) should be dots per CSS inch/centimeter/pixel, not per physical in/cm/px"
---
[CSS3 メディアクエリ](https://developer.mozilla.org/ja/docs/Web/CSS/Media_Queries) の仕様が更新され、[解像度の単位](https://developer.mozilla.org/ja/docs/Web/CSS/resolution) である `dpi`、`dpcm`、`dppx` が、物理単位ではなく CSS ピクセル単位のドットに相当するようになりました。Firefox の実装もこれに合わせて更新されました。
