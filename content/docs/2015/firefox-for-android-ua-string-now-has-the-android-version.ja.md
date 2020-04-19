---
title: "Android 版 Firefox の UA 文字列に Android のバージョンが含まれるようになりました"
date: "2015-06-13T15:20:46-04:00"
categories: ["networking"]
tags: []
versions: ["41", "45-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1169772"
      title: "Bug 1169772 - Add Android version number to Fennec UA String"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1174784"
      title: "Bug 1174784 - Youtube video playback broken with Android version in UA string"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1193354"
      title: "Bug 1193354 - play.google.com - No image appearing on Firefox for Android"
---
[Android 版 Firefox](https://developer.mozilla.org/Firefox_for_Android) のユーザーエージェント (UA) 文字列に、プラットフォームトークンの一部としてその端末の Android バージョンが含まれるようになりました。詳しくは [Gecko UA 文字列リファレンス](https://developer.mozilla.org/docs/Web/HTTP/Gecko_user_agent_string_reference#Android_%28version_41_and_above%29) を参照してください。あなたのサイトでモバイル向け UA 判定を行っている場合は、問題なく動作することを確認した方がいいでしょう。これまでのところ、*YouTube* での動画再生と *Google Play* での画像表示への影響が判明しています。
