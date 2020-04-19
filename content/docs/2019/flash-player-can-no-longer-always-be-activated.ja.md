---
title: "Flash Player を常に有効化することができなくなりました"
date: "2019-06-15T23:03:00-04:00"
categories: ["plugins"]
tags: []
releases: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1519434"
      title: "Bug 1519434 - Remove \"Always Activate\" and \"Remember this decision\" Flash options in Firefox 69"
---
現在進行中の [Flash プラグイン対応廃止](https://www.fxsitecompat.dev/ja/docs/2018/flash-plug-in-support-will-be-removed-in-2020/) の一環として、Firefox 69 でページ通知ダイアログから「常に有効化する」オプションが、アドオンマネージャーから「この選択を記憶する」オプションが、それぞれ削除されました。つまり今後、ブラウザーセッション中にウェブサイト上で Flash コンテンツを表示するかどうか Firefox が毎回ユーザーに尋ねることとなり、ユーザーはこの挙動を変更できません。

[Firefox Public Data Report](https://data.firefox.com/dashboard/hardware) によれば、本稿執筆時点で Firefox ユーザーの約半数しか Flash Player をインストールしておらず、その数は着実に減り続けています。2020 年には Flash 対応が Firefox やその他のブラウザーから削除されることを念頭に、まだあなたのサイトが旧式の動画プレーヤーなど何らかの Flash コンテンツに依存している場合は、できる限り早く移行計画を立てるよう強く推奨します。
