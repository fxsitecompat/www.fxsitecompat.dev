---
title: "トランジションとアニメーションに指定した負の継続時間は無視されるようになりました"
date: "2012-10-09T06:00:00-04:00"
categories: ["css"]
tags: []
releases: ["16"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=773102"
      title: "Bug 773102 – transition-duration and animation-duration should reject negative values at parse time"
---
[`transition-duration`](https://developer.mozilla.org/docs/Web/CSS/transition-duration)、[`animation-duration`](https://developer.mozilla.org/docs/Web/CSS/animation-duration) 各プロパティに負の値を指定した場合、従来は [初期値](https://developer.mozilla.org/docs/Web/CSS/initial_value) である `0s` と解釈されていましたが、今後は不正な値として見なされ、宣言自体が無視されます。
