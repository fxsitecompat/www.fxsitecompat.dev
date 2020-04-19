---
title: "`localStorage` の保存上限サイズが 5 MB に変更されました"
date: "2012-12-03T03:53:26-05:00"
categories: ["dom"]
tags: []
releases: ["18", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=776416"
      title: "Bug 776416 – Remove exceptions to 5MB quota rule in localStorage"
---
従来、オフラインストレージが有効になっているページでは最大で 200 MB のデータを保存することが可能でしたが、同期 IO を必要とする [`localStorage`](https://developer.mozilla.org/docs/DOM/Storage#localStorage) はパフォーマンスの問題を引き起こすことなどから、保存上限サイズ (クォータ) が 5 MB へ変更されました。また、ユーザーが Cookie を削除する際、`localStorage` に保存されているデータも併せて削除されるようになりました。今後はできる限り [`IndexedDB`](https://developer.mozilla.org/docs/IndexedDB) の非同期 API を使用することが推奨されています。
