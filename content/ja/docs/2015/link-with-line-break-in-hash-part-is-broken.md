---
title: "ハッシュ部分に改行を含むリンクが壊れています"
date: "2015-10-20T21:43:00-07:00"
categories: ["networking"]
tags: [""]
versions: "38"
statuses: "regressed"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1189852": "Bug 1189852 - link broken which a line break on hash part after Bug 1144398"
---
Firefox 39 以降で、`#` に続くフラグメントに改行コードが含まれる HTML リンクが動作しません。これは、そうした文字が URL 仕様で許可されておらず、ブラウザがその制約を強制するようになったためです。サイト互換性問題を防ぐため、この挙動は Firefox 42 で変更され、ハッシュ部分の `\r` (CR)、`\n` (LF)、`\t` (タブ) 文字が除去されるだけになりました。`\0` (ヌル文字) を含むリンクは引き続き拒絶されます。
