---
title: "HTTP/2 で未定義の疑似ヘッダフィールドが受け入れられなくなりました"
date: "2015-09-23T05:27:00-04:00"
categories: ["networking"]
tags: []
versions: ["42"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1136727"
      title: "Bug 1136727 - Firefox accepts undefined or invalid pseudo-header fields in HTTP/2"
---
Firefox 41 およびそれ以前のバージョンは、HTTP/2 レスポンスに含まれる未定義あるいは不正な疑似ヘッダフィールドを誤って受け入れていました。*Twitter* で `:version` フィールドが使われていましたが後に削除されています。Firefox 42 以降、[仕様](https://http2.github.io/http2-spec/index.html#HttpResponse) で必要とされている `:status` を除き、疑似ヘッダフィールドは受け入れられなくなり、任意のフィールドを含むレスポンスヘッダは不正な形式であると見なされます。
