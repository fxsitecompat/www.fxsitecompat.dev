---
title: "`window.open()` がイベントごとに一度しか呼び出せなくなりました"
date: "2018-12-21T00:52:00-05:00"
categories: ["dom"]
tags: []
versions: ["65"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=675574"
      title: "Bug 675574 - Do not allow more than one call to window.open() when we allow popups"
---
Firefox 65 で、複数のポップアップウィンドウが同時に開かれるのを防ぐため、ポップアップブロッカーが改良されました。`window.open` メソッドの呼び出しはイベントごとに 1 回のみ許容され、もし後続の呼び出しが行われた場合はブラウザーによってブロックされます。より良いユーザー体験のためには、いずれにしても複数ポップアップやタブを開くことは避けるべきでしょう。
