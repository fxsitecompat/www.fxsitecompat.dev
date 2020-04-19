---
title: "プラグイン対応は Flash を除き廃止されました"
date: "2016-10-04T00:57:00-07:00"
categories: ["plugins"]
tags: []
releases: ["52"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1269807"
      title: "Bug 1269807 - Remove support for all NPAPI plugins (except Flash)"
    - url: "https://www.mozilla.jp/blog/entry/10508/"
      title: "Firefox における NPAPI プラグインの取り扱いについて"
    - url: "https://groups.google.com/d/topic/mozilla.dev.tech.plugins/Cu1rOVEn45M/discussion"
      title: "Java plugin phase out timeline"
aliases:
    - "/ja/docs/2015/plug-in-support-will-be-dropped-by-the-end-of-2016-except-flash/"
---
長年にわたり、Mozilla はウェブ標準技術を強化することでウェブからプラグインをなくすことを目指してきました。プラグインは、ブラウザーのパフォーマンス、セキュリティ、ユーザー体験に悪影響を与えているためです。

[アニメーション効果](https://developer.mozilla.org/docs/Web/CSS/CSS_Animations/Using_CSS_animations)、[動画再生](https://developer.mozilla.org/docs/Web/Guide/HTML/Using_HTML5_audio_and_video)、[ドラッグ＆ドロップによるファイルアップロード](https://developer.mozilla.org/docs/Web/Guide/HTML/Drag_and_drop)、[クリップボード操作](https://hacks.mozilla.org/2015/09/flash-free-clipboard-for-the-web/) から、[インタラクティブな 3D ゲーム](https://games.mozilla.org/)、[リアルタイムビデオチャット](https://developer.mozilla.org/docs/Web/Guide/API/WebRTC) に至るまで、今ではあらゆることをプラグインなしで実現できます。Firefox は [組み込みの PDF リーダー](https://support.mozilla.org/kb/view-pdf-files-firefox-without-downloading-them) や [DRM 対応](https://support.mozilla.org/kb/enable-drm) も提供しています。

Microsoft は [Silverlight を廃止予定としました](https://support.microsoft.com/ja-jp/lifecycle?C2=12905)。Oracle からも 2016 年 1 月に [Java ブラウザープラグインの廃止予定](https://blogs.oracle.com/java-platform-group/entry/moving_to_a_plugin_free) が発表されました。2016 年 4 月時点で、Apple は [Windows 版 QuickTime のサポートを打ち切っています](https://support.apple.com/ja-jp/HT201175)。OS X 版の QuickTime プラグインは既に [10.9 Mavericks 以降無効化されています](https://support.apple.com/ja-jp/HT205081)。2016 年 7 月公開の Unity 5.4 で [Unity Web Player](https://blogs.unity3d.com/jp/2015/10/08/unity-web-player-roadmap/) プラグインへの対応は廃止されています。

そのため、[2015 年 10 月以降廃止予定となっていた](https://www.mozilla.jp/blog/entry/10508/) Firefox におけるレガシーな [NPAPI プラグイン](https://developer.mozilla.org/docs/Plugins) 対応は、まだ広く用いられている Adobe Flash Player を例外として Firefox 52 から削除されました。Windows 64 ビット版 Firefox では [既に対応プラグインが Flash と Silverlight のみとなっています](https://www.fxsitecompat.dev/ja/docs/2015/64-bit-firefox-for-windows-is-officially-available-flash-and-silverlight-are-the-only-supported-plug-ins/)。ウェブサイト運営者は、Java アプレットや Silverlight 動画など、すべてのプラグインコンテンツを代替技術で置き換える計画を立てなければなりません。

なお、特に Java を必要とする法人ユーザーのために、Firefox 52 [延長サポート版](https://www.mozilla.jp/business/) (ESR) では 2018 年 <del>5 月</del> <ins>8 月</ins> までプラグイン対応が維持されます。
