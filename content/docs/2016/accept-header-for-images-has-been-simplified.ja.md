---
title: "画像向け `Accept` ヘッダーが簡素化されました"
date: "2016-03-10T08:02:00-05:00"
categories: ["networking"]
tags: []
versions: ["47"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1249474"
      title: "Bug 1249474 - Accept header sent for images prevents w3.org from serving us SVG images in W3C's style sheet"
aliases:
    - "/ja/docs/2016/accept-header-for-images-has-been-changed/"
---
Firefox は従来、[画像向け `Accept` HTTP ヘッダーの値](https://developer.mozilla.org/docs/Web/HTTP/Content_negotiation/List_of_default_Accept_values#Values_for_an_image) として `image/png,image/*;q=0.8,*/*;q=0.5` を送信していました。PNG 画像の普及により現時点でこの値はさして意味をなさなくなったこと、また *W3C* のサイトで SVG の代わりに PNG 画像が Firefox に配信されてしまうという互換性問題が見つかったことから、Firefox 47 以降のバージョンは Safari と同様に `*/*` を送信するようになりました。Firefox が [WebP 画像形式に対応](https://bugzilla.mozilla.org/show_bug.cgi?id=856375) した場合には、おそらく `image/webp,*/*` に変更されます。
