---
title: "`canPlayType(\'video/webm\')` は `\'maybe\'` を返すようになりました"
date: "2013-12-09T02:32:17-05:00"
categories: ["audio-video"]
tags: []
releases: ["28", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=884275"
      title: "Bug 884275 – canPlayType(\'video/webm\') should report \'maybe\' instead of \'probably\'"
---
[`HTMLMediaElement`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) インターフェイスの `canPlayType` メソッドが仕様に準拠するため更新されました。Firefox が対応していないコーデックでメディアがエンコードされている可能性があるとして、`canPlayType('video/webm')` と `canPlayType('audio/webm')` は `'probably'` の代わりに `'maybe'` を返すようになりました。`type` 引数でコーデックが指定されている場合、このメソッドはコーデックに応じて `'probably'` もしくは `''` (空文字列) を返します。例えば、`canPlayType('video/webm; codecs=vp8')` は `'probably'` を返します。
