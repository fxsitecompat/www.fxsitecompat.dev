---
title: "CSP 実装が最終仕様に合わせて更新されました"
date: "2013-04-06T04:52:59-04:00"
categories: ["privacy-security"]
tags: []
versions: "23"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=746978": "Bug 746978 – sync CSP directive parsing and directive names with w3c CSP 1.0 spec"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=783049": "Bug 783049 – CSP : use existing/old parser for X-Content-Security-Policy header, new/CSP 1.0 spec compliant parser for Content-Security-Policy header"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=842657": "Bug 842657 – Flip the pref to enable the CSP 1.0 parser for Firefox"
---
[Content Security Policy (CSP)](https://developer.mozilla.org/ja/docs/Security/CSP) 1.0 の仕様が実装されました。ポリシーが `X-Content-Security-Policy` ヘッダで配信された場合は既存のパーサが使われ、ポリシーが公式仕様となった `Content-Security-Policy` ヘッダで配信された場合は 1.0 仕様に準拠した新しいパーサが使われます。詳しくは [Mozilla Security Blog の記事](https://blog.mozilla.org/security/2013/06/11/content-security-policy-1-0-lands-in-firefox/) をご覧ください。あなたのサイトで CSP を実装したい場合は最新の仕様を参照してください。[MDN 上のドキュメント](https://developer.mozilla.org/ja/docs/Security/CSP) も近々更新されるはずです。
