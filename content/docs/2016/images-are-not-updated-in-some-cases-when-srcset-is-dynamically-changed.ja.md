---
title: "`srcset` が動的に変更された際に画像が更新されない場合があります"
date: "2016-03-24T15:26:00-04:00"
categories: ["dom"]
tags: []
versions: ["45"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1259482"
      title: "Bug 1259482 - Product image not changing upon selection in Woocommerce/Wordpress"
aliases:
    - "/ja/docs/2016/images-are-not-updated-in-some-cases-when-srcset-is-modified/"
---
Firefox 38 で導入された [`srcset`](https://developer.mozilla.org/docs/Web/HTML/Element/img#attr-srcset) 属性を持つ [レスポンシブ画像](https://developer.mozilla.org/Learn/HTML/Multimedia_and_embedding/Responsive_images) が、その属性値が特定の方法でスクリプトにより変更された際、正しく更新されないというリグレッションが Firefox 45 で発生しました。このバグは *WooCommerce* を使用したオンラインストア上の製品画像表示に影響しています。Mozilla 開発者が解決策に取り組みます。

**更新**: 私たちの分析の結果、このバグは 9 万以上のアクティブインストールを抱える [*YITH WooCommerce Zoom Magnifier*](https://ja.wordpress.org/plugins/yith-woocommerce-zoom-magnifier/) プラグインに影響することが分かりました。

**更新**: Firefox 45.0.2 でパッチが当てられましたが、まだまれに問題が再現するとの報告が QA チームから上がっています。Mozilla 開発者が原因を調べています。
