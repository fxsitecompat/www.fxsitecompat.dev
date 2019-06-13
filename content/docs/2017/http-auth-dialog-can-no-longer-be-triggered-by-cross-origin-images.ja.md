---
title: "配信元が異なる画像から HTTP 認証ダイアログを表示できなくなりました"
date: "2017-12-06T14:19:00-05:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["59"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1357835"
      title: "Bug 1357835 - Add a pref to disable HTTP Auth on 3rd party images"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1423146"
      title: "Bug 1423146 - Do not allow an auth prompt requested by an image resource loaded from cross-origin"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/o1rWz3k1IxU/discussion"
      title: "Intent to ship: Do not allow a http-auth prompt requested by an image resource loaded from a cross-origin"
---
Firefox 59 以降、現在のページと異なる配信元から読み込まれた画像リソースが HTTP 認証ダイアログプロンプトを表示することはできなくなりました。これは、攻撃者が任意の画像を第三者のページへ埋め込むことができた場合にユーザーの認証情報が盗まれる恐れを防ぐための措置です。

このセキュリティ対策は元々 [Firefox 40](https://www.fxsitecompat.dev/ja/docs/2015/http-auth-dialog-can-no-longer-be-triggered-by-cross-origin-resources/) で導入されましたが、いくつかの互換性問題によりすぐバックアウトされていました。一部の組織では認証ダイアログを表示するためクロスオリジンのフレームやスクリプトがまだ使われている可能性はありますが、画像は正規の手法とは考えられないため、今回の変更が実施されました。Google Chrome が既に同じ変更を実装していることから、特に影響はないと Mozilla 開発者は見ています。
