---
title: "ウェブページ内での FTP リソースの読み込みが許容されなくなりました"
date: "2018-04-06T20:32:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1404744"
      title: "Bug 1404744 - Block ftp subresource requests inside http(s) pages"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/HzumeW2JQW8/discussion"
      title: "Intent to implement and ship: Blocking FTP subresources"
---
Firefox 61 以降、HTTP(S) ページによる FTP サーバーからのリソース読み込みがブロックされるようになります。このセキュリティ対策は主に `src="ftp://..."` を伴った `<img>`、`<script>`、`<iframe>` 要素に影響します。こうした FTP リソースは、ブラウザー内や FTP ページ内で直接開かれた場合は引き続き読み込むことが可能であり、FTP サーバーへのリンクも同様にブロックされません。[Google Chrome](https://www.chromestatus.com/feature/5709390967472128) が 2017 年 6 月に公開されたバージョン 59 で既にこの変更を行っていることから、互換性リスクは低いはずです。

Firefox の FTP 対応は、その安全性の問題から将来的に廃止予定とされる可能性がありますが、今のところ具体的なスケジュールは決まっていません。
