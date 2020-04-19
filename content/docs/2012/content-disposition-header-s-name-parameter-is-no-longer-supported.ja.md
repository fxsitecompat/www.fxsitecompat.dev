---
title: "`Content-Disposition` ヘッダーの `name` パラメーターは非対応となりました"
date: "2012-12-03T03:54:45-05:00"
categories: ["misc"]
tags: []
versions: ["19", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=776339"
      title: "Bug 776339 – remove support of Content-Disposition \"name\" parameter"
---
ファイルダウンロード時に使用される HTTP `Content-Disposition` ヘッダーに含まれる `name` パラメーターは無視されるようになりました。このパラメーターは非標準で、Firefox と Google Chrome しか対応していませんでした。今後は標準の `filename` パラメーターを使用してください。
