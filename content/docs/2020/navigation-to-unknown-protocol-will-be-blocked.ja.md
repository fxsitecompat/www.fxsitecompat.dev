---
title: "未知のプロトコルへのページ遷移はブロックされます"
date: "2020-04-07T02:02:00-04:00"
categories: ["dom"]
tags: []
releases: ["76"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1528305"
      title: "Bug 1528305 - Behavior on meta and location.href redirects to an unknown protocol can break pages."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/AaXUQ_t51D4/discussion"
      title: "Intent to implement and ship: Ignore navigation to unknown protocol"
---
Firefox は従来、ウェブページが `location.href`、`<meta http-equiv="refresh">` あるいはそれと類似した方法を使って未知のプロコトルへ遷移しようとすると、「アドレスのプロトコルが不明です」といったエラーページを表示していました。この挙動は独自の外部アプリケーションを開こうとする様々なサイトにおいてユーザー体験の問題を引き起こしていました。

Firefox 76 以降、そうしたページ遷移・リダイレクトは Google Chrome のように無視され、ウェブコンソールに「未知のプロコトルにより ... への遷移は中止されました」といった警告が記録されます。

外部アプリケーションを起動する必要がある場合や、単に外部アプリケーションがインストールされているかどうかを確認したい場合は、代わりに `window.open()` あるいは `<iframe>` のいずれかを使用できます。
