---
title: "Ogg メディア向け `X-Content-Duration` ヘッダの対応が打ち切られました"
date: "2015-09-15T23:38:00-04:00"
categories: ["audio-video", "networking"]
tags: []
versions: "41"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1160695": "Bug 1160695 - Clean up duration tracking and use mirroring for cross-thread access"
---
Web サーバがブラウザに Ogg 形式メディアの再生時間を伝えるために使用できる [`X-Content-Duration` HTTP ヘッダ](https://developer.mozilla.org/ja/docs/Web/HTTP/Configuring_servers_for_Ogg_media#Serve_X-Content-Duration_headers) は、あまり普及しておらず維持にも手間が掛かることから、Firefox による対応が打ち切られました。その代わり、[Ogg メディアのキーフレームインデックス](http://blog.pearce.org.nz/2010/08/keyframe-indexed-ogg-files-supported-in.html) が提供されている場合、Firefox はストリームの最後までシークせずに再生時間を特定することが可能です。
