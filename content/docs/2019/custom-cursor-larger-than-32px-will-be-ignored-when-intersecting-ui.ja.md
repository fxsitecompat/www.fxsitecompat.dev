---
title: "32px より大きい独自カーソルは UI 上では無視されるようになります"
date: "2019-05-13T14:47:00-04:00"
categories: ["css"]
tags: []
versions: ["67", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1445844"
      title: "Bug 1445844 - Custom cursor goes outside the bounds of the web content in \"malware\" website"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1534761"
      title: "Bug 1534761 - Change maximum cursor size when intersecting UI to 32 pixels."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/ke-KMmY1Mak/discussion"
      title: "Intent to Ship: Ignore custom cursors over 32 pixels intersecting UI"
---
CSS `cursor` プロパティを使うことで、ウェブサイトはマウスポインターのスタイルを所定の形式のいずれかか独自の画像に変えることができます。大抵の使用例は正当なものですが、一部の悪質なサイトがこの機能を悪用してカーソルを乗っ取り、ユーザーにブラウザーのタブを閉じさせないようにすることが知られています。

こうしたユーザー体験の問題を防ぐため、Firefox 67 以降、32 ピクセルよりも大きい独自カーソル画像は、ブラウザーの UI と交差している間は無視され、既定のカーソルに置き換えられます。ウェブ開発者は、特にゲームのために、コンテンツエリア内では今後も大きい独自カーソルを使うことが可能です。

Google も [Chrome 75](https://bugs.chromium.org/p/chromium/issues/detail?id=880863) で同様の変更を行っています。
