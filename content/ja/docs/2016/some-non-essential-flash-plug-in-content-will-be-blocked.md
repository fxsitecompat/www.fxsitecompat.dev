---
title: "一部の重要でない Flash プラグインコンテンツがブロックされるようになります"
date: "2016-08-20T16:36:00-04:00"
categories: ["plugins"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1275591"
      title: "Bug 1275591 - Enable plugin content blocking by default"
    - url: "https://www.mozilla.jp/blog/entry/10554/"
      title: "Firefox 内での Adobe Flash 使用量を削減します"
---
Firefox は、継続中の [NPAPI プラグイン廃止](https://www.fxsitecompat.com/ja/docs/2015/plug-in-support-will-be-dropped-by-the-end-of-2016-except-flash/) の一環として、不必要な Flash コンテンツに重点を置いたプラグインブロックリストを実装しました。ブラウザのパフォーマンス、安定性、セキュリティ向上が狙いです。Web ページに埋め込まれた不可視 Flash ピクセルを主に含んだ [ブロックリスト](https://github.com/mozilla-services/shavar-plugin-blocklist) は、サイト互換性問題に気を配りつつ徐々に拡大されていく予定です。詳しくは [この Future Releases ブログの記事](https://www.mozilla.jp/blog/entry/10554/) を参照してください。
