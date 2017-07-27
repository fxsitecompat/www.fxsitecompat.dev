---
title: "参考: SSL ページでの非 SSL コンテンツの読み込みを禁止する設定が追加されました"
date: "2012-12-03T03:53:26-05:00"
categories: ["privacy-security"]
tags: []
versions: ["18"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=62178"
      title: "Bug 62178 – implement mechanism to prevent sending insecure requests from a secure context"
---
SSL (`https`) 使用ページ内で非 SSL (`http`) サイトからコンテンツが読み込まれるのをブロックする設定が追加されました。スクリプト、スタイルシート、プラグインコンテンツ、インラインフレーム、[ウェブフォント](https://developer.mozilla.org/ja/docs/CSS/@font-face)、[WebSockets](https://developer.mozilla.org/ja/docs/WebSockets) は `security.mixed_content.block_active_content` で、それ以外の画像、[音声](https://developer.mozilla.org/ja/docs/HTML/Element/audio)、[動画](https://developer.mozilla.org/ja/docs/HTML/Element/video) といった静的コンテンツは `security.mixed_content.block_display_content` で、それぞれブロックすることが可能です。

初期設定は今のところいずれも無効 (`false`) となっていますが、ユーザーがこの設定を有効にした場合、該当するコンテンツは読み込まれなくなります。また、設定項目のうち `security.mixed_content.block_active_content` は、Firefox の将来のバージョンで [初期設定で有効となる](https://bugzilla.mozilla.org/show_bug.cgi?id=834836) 予定です。サイト運営者は SSL ページに非 SSL コンテンツを混在させないよう注意しましょう。
