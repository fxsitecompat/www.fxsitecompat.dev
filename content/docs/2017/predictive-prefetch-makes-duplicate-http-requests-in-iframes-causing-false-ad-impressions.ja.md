---
title: "予測先読み機能が iframe 内で重複 HTTP リクエストを行い、誤った広告インプレッションを発生させます"
date: "2017-03-30T11:38:00-04:00"
categories: ["networking"]
tags: []
releases: ["52", "52-esr"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1349921"
      title: "Bug 1349921 - Cached iframe executes previously loaded and dynamically inserted scripts, makes network calls before \"onload\" event."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1350032"
      title: "Bug 1350032 - Google seeing duplicate requests to custom URIs that should only be requested once"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1351082"
      title: "Bug 1351082 - System addon to disable predictive prefetch"
    - url: "https://mail.mozilla.org/pipermail/gofaster/2017-March/000655.html"
      title: "Intent to implement & ship: disable network predictor prefetch"
---
Firefox 52 ユーザーからの大量の重複インプレッションが観測されているという報告が、複数のオンライン広告ネットワーク企業から Mozilla へ寄せられました。この問題は、新たに有効化されたネットワーク予測先読みサービスのバグによるもので、インラインフレーム内で動的に挿入されたスクリプトや画像の URL へさえも繰り返し GET リクエストが行われてしまうことが判明しました。

この予測先読み機能は、Firefox 52 ではまもなくリモートから無効化され、問題の調査と解決が済み次第、Firefox 55 で再度有効化される予定です。
