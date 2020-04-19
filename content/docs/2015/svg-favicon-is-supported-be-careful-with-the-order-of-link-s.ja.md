---
title: "SVG サイトアイコンに対応、ただし `<link>` の順番には注意が必要です"
date: "2015-06-13T15:20:46-04:00"
categories: ["html"]
tags: []
releases: ["41", "45-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=366324"
      title: "Bug 366324 - SVG site icons (favicons, shortcut icons) support"
---
Firefox 41 では、長く待ち望まれていた [SVG](https://developer.mozilla.org/docs/Web/SVG) 形式サイトアイコン (ファビコン) への対応が追加されました。これはうまく機能するはずですが、ファビコンのための [`<link>`](https://developer.mozilla.org/docs/Web/HTML/Element/link) 要素の順番には気をつける必要があります。[*Flickr*](https://bugzilla.mozilla.org/show_bug.cgi?id=1181681)、[*Pinterest*](https://bugzilla.mozilla.org/show_bug.cgi?id=1174568)、[*Twitter*](https://bugzilla.mozilla.org/show_bug.cgi?id=1174552)、[*Yelp*](https://bugzilla.mozilla.org/show_bug.cgi?id=1174548) など一部の人気サイトでは、本来意図された色付き通常ファビコンの代わりに、Safari 9 のピン留めタブ向けに用意された黒い SVG アイコンが Firefox 41 上で表示されてしまっていることが分かっています。この不一致は、それらのサイトが黒いアイコンを他のアイコンの「後」に配置しており、Firefox は HTML ソース内で指定された最後のアイコンを使用するために発生しています。回避策は、言うまでもありませんが、[Apple が推奨している通り](https://developer.apple.com/library/safari/releasenotes/General/WhatsNewInSafari/Articles/Safari_9.html#//apple_ref/doc/uid/TP40014305-CH9-SW20)、Safari 向けの黒い SVG アイコンを他のアイコンの「前」に持ってくることです。
