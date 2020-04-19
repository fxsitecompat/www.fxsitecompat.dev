---
title: "CSP 実装が最終仕様に合わせて更新されました"
date: "2013-04-06T04:52:59-04:00"
categories: ["privacy-security"]
tags: []
releases: ["23", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=746978"
      title: "Bug 746978 – sync CSP directive parsing and directive names with w3c CSP 1.0 spec"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=783049"
      title: "Bug 783049 – CSP : use existing/old parser for X-Content-Security-Policy header, new/CSP 1.0 spec compliant parser for Content-Security-Policy header"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=842657"
      title: "Bug 842657 – Flip the pref to enable the CSP 1.0 parser for Firefox"
---
[Content Security Policy (CSP)](https://developer.mozilla.org/docs/Security/CSP) 1.0 の仕様が実装されました。ポリシーが `X-Content-Security-Policy` ヘッダーで配信された場合は既存のパーサーが使われ、ポリシーが公式仕様となった `Content-Security-Policy` ヘッダーで配信された場合は 1.0 仕様に準拠した新しいパーサーが使われます。詳しくは [Mozilla Security Blog の記事](https://blog.mozilla.org/security/2013/06/11/content-security-policy-1-0-lands-in-firefox/) をご覧ください。あなたのサイトで CSP を実装したい場合は最新の仕様を参照してください。[MDN 上のドキュメント](https://developer.mozilla.org/docs/Security/CSP) も近々更新されるはずです。
