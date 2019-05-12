---
title: "外部プロトコル URL の `<iframe>` への読み込みがブロックされるようになりました"
date: "2019-02-18T21:28:00-05:00"
categories: ["misc"]
tags: []
versions: ["67"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=167475"
      title: "Bug 167475 - [URL] Disable external and returning no data protocol handlers in all cases, excluding <A HREF=>"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1514547"
      title: "Bug 1514547 - Can't open roblox"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1522181"
      title: "Bug 1522181 - external protocol URLs blocking should be behind pref"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1527882"
      title: "Bug 1527882 - Enable the blocking of external protocol URLs in iframes"
---
Firefox 66 以降、サービス妨害 (DoS) のような攻撃を防ぐため、何らデータを返さない外部プロトコル URL を `<iframe>` に読み込むことはできなくなりました。影響を受けるプロトコルには、以下に示すように、メールクライアントを開く目的で使用可能な `mailto` が含まれます。

```html
<!-- こうした URL は今後ブロックされます -->
<iframe src="mailto:support@example.com"></iframe>
<iframe src="ircs://irc.mozilla.org/firefox"></iframe>
<iframe src="itms://itunes.apple.com/us/app/apple-store/id989804926"></iframe>
```

`<a href="mailto:...">` といった通常のリンクや `location.href='mailto:...'` といった JavaScript コードは引き続き動作します。

**更新**: この変更は Mozilla 開発者がサイト互換性問題に対処できるよう [Firefox 67](https://bugzilla.mozilla.org/show_bug.cgi?id=1527882) へ延期されました。
