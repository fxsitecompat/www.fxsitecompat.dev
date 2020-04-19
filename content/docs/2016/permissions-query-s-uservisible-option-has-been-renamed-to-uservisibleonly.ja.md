---
title: "`Permissions.query()` の `userVisible` オプションが `userVisibleOnly` に改名されました"
date: "2016-04-24T06:34:00-04:00"
categories: ["dom"]
tags: []
versions: ["48", "52-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1261405"
      title: "Bug 1261405 - PushPermissionDescriptor in Permissions.webidl is wrong ('userVisible' should be 'userVisibleOnly')"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1250902"
      title: "Bug 1250902 - Push notifications from http://simple-push-demo.appspot.com/ stopped working"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1266821"
      title: "Bug 1266821 - Remove PushPermissionDescriptor from the Permissions API"
---
Firefox 46 と 47 でそれぞれ実装された [`Permissions.query`](https://developer.mozilla.org/docs/Web/API/Permissions/query)、[`revoke`](https://developer.mozilla.org/docs/Web/API/Permissions/revoke) 両メソッドの `userVisible` オプションが、最新の Push API 仕様に従って `userVisibleOnly` に改名されました。

Firefox は実際のところ `userVisibleOnly` が `true` に設定されていた場合に例外 `NS_ERROR_NOT_IMPLEMENTED` を投げます。これは、Firefox が Google Chrome と異なり、このオプションではなく独自のクォータシステムを採用しているためです。あるデモアプリがこの変更の影響を受けています。このオプションが例外を投げる代わりに単に無視されるよう、`PushPermissionDescriptor` 対応自体を Firefox から削除する予定があります。

**更新**: `userVisibleOnly` オプションを必須している Google Chrome との互換性のため、`PushPermissionDescriptor` ディクショナリは [削除され](https://bugzilla.mozilla.org/show_bug.cgi?id=1266821)、Firefox ではこのオプションは単に無視されるようになりました。
