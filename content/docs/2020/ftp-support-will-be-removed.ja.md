---
title: "FTP 対応が廃止されます"
date: "2020-04-10T02:21:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1570155"
      title: "Bug 1570155 - How many people use FTP?"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1574475"
      title: "Bug 1574475 - Remove FTP support"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1622409"
      title: "Bug 1622409 - Put FTP code behind a pref"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/FqCZUT9ay_o/discussion"
      title: "Intent to unship: FTP protocol implementation"
---
セキュリティ上の理由から、Mozilla は 2021 年に Firefox の FTP サポートを廃止する予定です。FTP は安全でないプロトコルで、現時点で使用率は非常に低くなっています (Mozilla によれば 0.05%)。Firefox の非常に古い実装を維持するのは困難であり、FTPS 対応が追加される予定もありません。

Firefox 77 以降、Nightly チャンネルでは FTP 対応が無効化されます。プロトコルは単体の FTP クライアントやファイルマネージャーといった外部アプリケーションによって処理されます。

なお、[Google](https://www.chromestatus.com/feature/6246151319715840) も Chrome ブラウザーの FTP 対応を廃止予定としています。COVID-19 の世界的流行により具体的な廃止スケジュールは定まっていませんが、もしあなたが FTP サーバーを運用している場合は、ウェブサーバーから HTTPS を通じてファイルを配信することを検討してください。
