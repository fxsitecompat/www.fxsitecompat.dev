---
title: "4 週間後に公開の Firefox 66 では、メディアの自動再生がブロックされ、ページ読み込み中にタイマーが先送りされます"
date: "2019-02-20T22:07:00-05:00"
---
少々遅くなってしまいましたが、私たちは 2019 年 2 回目のリリースに向けて復帰してきました。

[Firefox 66 Beta と Developer Edition](https://www.mozilla.org/firefox/channel/desktop/) がこれまで数週間にわたって公開されています。ホリデーシーズンのため変更はそれほど多くありませんが、[メディア自動再生のブロック](https://www.fxsitecompat.com/ja/docs/2019/audible-media-s-autoplay-is-now-blocked-by-default/) や [`setTimeout()` 遅延](https://www.fxsitecompat.com/ja/docs/2019/settimeout-and-setinterval-are-now-deferred-during-page-load/) といったいくつかのことが皆さんのサイトに影響を及ぼす可能性があります。元々 Firefox 65 向けに予定されていた [`window.event` と `Event.returnValue` への対応](https://www.fxsitecompat.com/ja/docs/2018/support-for-window-event-and-event-returnvalue-has-been-added-again/) もリストに載っています。

すべての [Firefox 66 互換性情報](https://www.fxsitecompat.com/ja/versions/66/) を確認して、3 月 19 日公開の最終版に備えましょう。
