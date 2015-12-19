---
title: "プラグイン対応は Flash を除き 2016 年末までに廃止されます"
date: "2015-10-25T14:07:00-07:00"
categories: ["plugins"]
tags: []
versions: ["future"]
statuses: "affected"
references:
    "http://www.mozilla.jp/blog/entry/10508/": "Firefox における NPAPI プラグインの取り扱いについて"
---
長年にわたり、Mozilla は Web 標準技術を強化することで Web からプラグインをなくすことを目指してきました。プラグインは、ブラウザのパフォーマンス、セキュリティ、ユーザ体験に悪影響を与えているためです。[アニメーション効果](https://developer.mozilla.org/ja/docs/Web/CSS/CSS_Animations/Using_CSS_animations)、[動画再生](https://developer.mozilla.org/ja/docs/Web/Guide/HTML/Using_HTML5_audio_and_video)、[ドラッグ＆ドロップによるファイルアップロード](https://developer.mozilla.org/ja/docs/Web/Guide/HTML/Drag_and_drop)、[クリップボード操作](https://hacks.mozilla.org/2015/09/flash-free-clipboard-for-the-web/) から、[インタラクティブな 3D ゲーム](https://developer.mozilla.org/ja/docs/Games)、[リアルタイムビデオチャット](https://developer.mozilla.org/ja/docs/Web/Guide/API/WebRTC) に至るまで、今ではあらゆることをプラグインなしで実現できます。Firefox は [組み込みの PDF リーダー](https://support.mozilla.org/ja/kb/view-pdf-files-firefox-without-downloading-them)、[DRM 対応](https://support.mozilla.org/ja/kb/enable-drm)、[実験的 Flash 代替技術](https://developer.mozilla.org/ja/docs/Mozilla/Projects/Shumway) も提供しています。

そのため、時代遅れとなった [NPAPI プラグイン](https://developer.mozilla.org/ja/docs/Plugins) 対応は、Adobe Flash Player を例外として 2016 年末までに Firefox から削除されることになりました。Windows 64 ビット版 Firefox では [対応プラグインは Flash、Silverlight のみとなります](https://www.fxsitecompat.com/ja/docs/2015/64-bit-firefox-for-windows-is-officially-available-flash-and-silverlight-are-the-only-supported-plug-ins/)。Web サイト運営者は、すべてのプラグインコンテンツを代替技術で置き換える計画を立てなければなりません。詳しくは [Mozilla の発表](http://www.mozilla.jp/blog/entry/10508/) を参照してください。
