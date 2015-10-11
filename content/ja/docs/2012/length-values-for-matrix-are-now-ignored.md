---
title: "`matrix()` に指定した長さの値は無視されるようになりました"
date: "2012-10-09T06:00:00-04:00"
categories: ["css"]
tags: []
versions: "16"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=719054": "Bug 719054 – matrix() and matrix3d() with length units should be parse errors"
---
`matrix`、`matrix3d` の両 [トランスフォーム関数](https://developer.mozilla.org/ja/docs/Web/CSS/transform-function) について、Firefox はこれまで、長さの値、すなわち `10px` のような単位付きの値を誤って受け入れていました。この挙動が仕様に合わせて修正され、長さの値が指定された場合はパースエラーを返すようになりました。
