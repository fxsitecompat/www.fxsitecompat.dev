---
title: "Firefox のロケーションバーが安全でないサイトに対して壊れた南京錠アイコンを表示するようになりました"
date: "2019-07-21T21:13:00-04:00"
categories: ["privacy-security"]
tags: []
releases: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1562881"
      title: "Bug 1562881 - [Protections Panel] Remove \"i\" icon and make the shield icon persistent on the URL bar."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/RzmOHmoksdU/discussion"
      title: "Intent to Ship: Show an indicator for insecure HTTP in the URL bar"
    - url: "https://blog.mozilla.org/security/2019/10/15/improved-security-and-privacy-indicators-in-firefox-70/"
      title: "Mozilla Security Blog: Improved Security and Privacy Indicators in Firefox 70"
---
現在進行中の [安全でない HTTP 廃止](https://www.fxsitecompat.dev/ja/docs/2015/insecure-http-will-be-deprecated/) の一環として、Firefox 70 以降、ユーザーが安全でないサイトを訪れるたびに、ロケーションバー内に壊れた南京錠アイコンが表示されるようになります。これは既に「保護されていません」ラベルを表示している [Google Chrome](https://www.blog.google/products/chrome/milestone-chrome-security-marking-http-not-secure/) や [Safari](https://support.apple.com/en-us/HT208672) と同様の措置です。

<img src="/images/screenshots/1562881-insecure-icon.png" width="160" height="80" alt="">

これは実際のところサイト互換性に何ら影響を与えるものではありませんが、より良いセキュリティとユーザー体験のために、ウェブマスターの皆さんにはサイトを HTTPS で配信するよう強く推奨します。
