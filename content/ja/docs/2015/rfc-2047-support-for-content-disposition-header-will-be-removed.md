---
title: "`Content-Disposition` ヘッダの RFC 2047 対応が削除されます"
date: "2015-10-27T14:25:00-07:00"
categories: ["networking"]
tags: []
versions: ["future"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=601933"
      title: "Bug 601933 - remove RFC 2047 encoding support for HTTP header field parameters"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=875615"
      title: "Bug 875615 - Revert to decoding RFC 2047-encoding until we have telemetry on usage"
---
Firefox は HTTP `Content-Disposition` ヘッダ内の `filename` パラメータを RFC 2047 エンコーディングを使用してデコードしようと試みます。仕様によればこれはバグであり、Firefox と Google Chrome にしか実装されていません。そのため、RFC 2047 対応は削除が検討されています。この変更は [元々 Firefox 22 で予定されていました](https://www.fxsitecompat.com/ja/docs/2013/rfc-2047-encoding-support-for-http-header-field-parameters-has-been-removed/) が、相互運用性問題のため延期されています。RFC 2231、5987 エンコーディングを代わりに使うべきです。
