---
title: "非同期レンダリングモードにより一部の Flash コンテンツの表示に問題が発生しています"
date: "2016-10-24T09:51:00-04:00"
categories: ["plugins"]
tags: []
versions: ["49"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1229961"
      title: "Bug 1229961 - Enable direct plugin drawing by default"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1305135"
      title: "Bug 1305135 - Flash 23 isn't using async rendering mode on release channels"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1307108"
      title: "Bug 1307108 - Enable async rendering by default on 49 using a system addon"
---
[Firefox 49.0.2](https://www.mozilla.org/firefox/49.0.2/releasenotes/) で、ブラウザーの安定性とパフォーマンスを向上させるため、Adobe Flash Player プラグインの非同期レンダリングが初期設定で有効となりました。これにより、64-bit 版 Windows 上での [Stage 3D 対応](https://www.fxsitecompat.dev/ja/docs/2016/flash-is-forced-windowless-mode-on-firefox-for-64-bit-windows-affecting-stage-3d/)、[入力メソッド (IME)](https://bugzilla.mozilla.org/show_bug.cgi?id=1301486)、ページスクロールに関する既知の問題も解決されました。

ただ、動画プレーヤーやゲームなど [様々なコンテンツが正常に表示されていないという報告](https://bugzilla.mozilla.org/showdependencytree.cgi?id=1229961&maxdepth=1&hide_resolved=0) があり、Mozilla 開発者がそれらの問題を調査しています。

**更新**: 相当数のリグレッションが発生したため、非同期プラグインレンダリングは Firefox 49 の Windows 32 ビット版ではまもなく [リモートで無効化](https://bugzilla.mozilla.org/show_bug.cgi?id=1312528) されます。Firefox 50 Beta でも無効化されました。一方 64 ビット版では、上記の問題を防ぐため有効のままとなります。
