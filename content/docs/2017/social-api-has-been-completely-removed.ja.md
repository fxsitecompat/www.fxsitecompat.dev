---
title: "Social API が完全に廃止されました"
date: "2017-08-17T11:17:00-04:00"
categories: ["misc"]
tags: []
versions: ["57"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1388902"
      title: "Bug 1388902 - Shut down the last of socialapi"
    - url: "https://mail.mozilla.org/pipermail/firefox-dev/2017-August/005709.html"
      title: "Intent to remove SocialAPI Share"
---
ブラウザーと [ソーシャルメディアサービス](https://activations.cdn.mozilla.net/ja/) の統合を可能にしていた Mozilla の非標準 [Social Share API](https://developer.mozilla.org/ja/docs/Mozilla/Projects/Social_API/Share) は、あまり使用されていないため Firefox 57 で削除されました。[Social API](https://developer.mozilla.org/ja/docs/Mozilla/Projects/Social_API) セットの大半は、この共有機能を除き、既に [Firefox 51](https://www.fxsitecompat.com/ja/docs/2016/social-api-has-been-removed-except-the-sharing-functionality/) で削除されています。サービスプロバイダーには、ブラウザーから直接行われるユーザーエンゲージメントを促すため、代わりに [ブラウザー拡張機能](https://developer.mozilla.org/ja/Add-ons/WebExtensions) を提供することが推奨されます。
