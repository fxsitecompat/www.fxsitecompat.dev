---
title: "WebGL のポイントスプライトが特定の環境で正しく描画されません"
date: "2016-04-29T05:20:00-04:00"
categories: ["canvas-webgl"]
tags: []
releases: ["46"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1268096"
      title: "Bug 1268096 - WebGL point sprites malfunctions in Firefox 46 on Windows D3D11 ANGLE"
---
ANGLE ライブラリの古い、リグレッションを含んだバージョンが原因で、Windows 7 と Windows Server 2008 R2 でポイントスプライト、具体的にはパーティクル効果が描画されないという WebGL のリグレッションが Firefox 46 で発生しました。この問題は ANGLE のアップストリーム修正を取り込むことによって修正されます。

**更新**: このバグは Firefox 47 Beta で修正されました。
