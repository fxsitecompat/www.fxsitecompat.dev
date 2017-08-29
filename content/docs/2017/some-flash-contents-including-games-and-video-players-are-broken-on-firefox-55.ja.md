---
title: "Firefox 55 でゲームや動画プレーヤーなど一部の Flash コンテンツが正常に動作しません"
date: "2017-08-29T19:02:00-04:00"
categories: ["plugins"]
tags: []
versions: ["55"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1340934"
      title: "Bug 1340934 - Re-enable Flash async drawing"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1393352"
      title: "Bug 1393352 - flash player: Font white on white background"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1394105"
      title: "Bug 1394105 - Firefox 55 - performance of Shockwave Flash content has dropped significantly, with web based flash running very slowly, disabling async drawing solves the issue"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1394408"
      title: "Bug 1394408 - [meta] tab switching bugs related to async painting"
---
Windows 版 Firefox 55 で Flash プラグインコンテンツの非同期描画が有効化されました。この変更は一般的にブラウザーのパフォーマンスを向上させますが、一方で、テキストが白文字になる、パフォーマンスが極端に低下する、タブ切り替え時に応答が止まるといったリグレッションがいくつか報告されています。すべての Flash サイトやユーザーが影響を受けるわけではなく、一部の人は [Flash のハードウェアアクセラレーションを有効化](https://forums.adobe.com/thread/891337) することで既に問題を解決しています。また、Firefox の Windows 64 ビット版は影響を受けないようです。Mozilla 開発者が根本原因を調査しています。
