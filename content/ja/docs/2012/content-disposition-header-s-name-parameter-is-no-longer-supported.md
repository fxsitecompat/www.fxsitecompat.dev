---
title: "`Content-Disposition` ヘッダの `name` パラメータは非対応となりました"
date: "2012-12-03T03:54:45-05:00"
categories: ["file-handling"]
tags: []
versions: ["19"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=776339"
      title: "Bug 776339 – remove support of Content-Disposition \"name\" parameter"
---
ファイルダウンロード時に使用される HTTP `Content-Disposition` ヘッダに含まれる `name` パラメータは無視されるようになりました。このパラメータは非標準で、Firefox と Google Chrome しか対応していませんでした。今後は標準の `filename` パラメータを使用してください。
