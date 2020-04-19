---
title: "絶対 DNS ID や不規則なワイルドカードを使った証明書の対応が廃止されました"
date: "2015-01-16T09:37:54-05:00"
categories: ["privacy-security"]
tags: []
versions: ["37", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1107790"
      title: "Bug 1107790 – Remove support for absolute hostnames in presented DNS IDs and name constraints"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1107791"
      title: "Bug 1107791 – Limit wildcard DNS ID support to names of the form *.example.com (not foo*.example.com)"
---
`example.com.` のように末尾にドットが付く絶対提示 DNS ID 構文を使った証明書は有効と認められなくなりました。また、ワイルドカード DNS ID 対応が `*.example.com` 形式に限定され、`foo*.example.com` や `*foo.example.com` といった他の形式には今後対応しません。
