---
title: "HTTP ヘッダフィールド項目の RFC 2047 エンコーディング対応が削除されました"
date: "2013-02-24T03:44:31-05:00"
categories: ["file-handling"]
tags: []
versions: "22"
statuses: "reverted"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=601933": "Bug 601933 – remove RFC 2047 encoding support for HTTP header field parameters"
---
`Content-Disposition` ヘッダ内の `filename` パラメータをデコードする際、Firefox は RFC 2047 エンコーディングを使用してエスケープを試みていました。これは関連仕様によるとバグであり、Firefox と Chrome でしか実装されていませんでした。RFC 2231、RFC 5987 エンコーディングで代用してください。

<ins>更新: RFC 2047 エンコーディングの使用状況についてデータを収集・解析するため、[**この変更は延期されました**](https://bugzilla.mozilla.org/show_bug.cgi?id=875615)。</ins>
