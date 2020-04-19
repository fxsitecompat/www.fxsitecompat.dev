---
title: "`X-Content-Type-Options: nosniff` がトップレベルドキュメントにも適用されたことで、一部のページがダウンロードされてしまいます"
date: "2019-10-21T19:11:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
releases: ["72"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1580607"
      title: "Bug 1580607 - Logout from Office365 causes download dialog box"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1582671"
      title: "Bug 1582671 - Firefox Treats Arris Modem Webpages (application/x-unknown-content-type) As Files to Download"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1587448"
      title: "Bug 1587448 - Enable XTCO-nosniff for FF 71"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1592651"
      title: "Bug 1592651 - Disable Pref respect_document_nosniff for Firefox 71"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1591932"
      title: "Bug 1591932 - Enable Content-Type Sniffing when no Type is provided and Xtco-Nosniff is set"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1592975"
      title: "Bug 1592975 - 2.99 - 8.02% raptor-tp6-instagram-firefox-cold / raptor-tp6-instagram-firefox-cold fcp / raptor-tp6-twitch-firefox fcp ..."
---
[`X-Content-Type-Options`](https://developer.mozilla.org/docs/Web/HTTP/Headers/X-Content-Type-Options) HTTP レスポンスヘッダーは Firefox 50 以降使用可能となっており、その `nosniff` ディレクティブを使うことで、間違った MIME タイプで配信されているスクリプトやスタイルシートを効果的にブロックすることができます。

Firefox 71 以降、ブラウザーセキュリティのさらなる向上を目的として、この対応がトップレベルドキュメントにも適用されます。つまり、`X-Content-Type-Options` ヘッダーが活用されている場合、`text/html` 以外の MIME タイプで配信された HTML ウェブページは、レンダリングされる代わりにダウンロードされることになります。

*Microsoft Office 365* を含め、この変更の影響を受ける既知のサイトがいくつかあるため、あなたのサイトも必ず再確認しましょう。

**更新**: この変更は Firefox 71 からバックアウトされました。Mozilla 開発者は微調整を行いつつ Firefox 72 で再度変更を行う計画を立てています。

**更新 2**: この変更は Firefox 72 へ再度投入されました。互換性リスクを緩和するため、`X-Content-Type-Options` が設定されているものの `Content-Type` が定義されていない場合は MIME タイプの自動判別が有効となります。

**更新 3**: 空の `Content-Type` 回避策は [Firefox 75](https://www.fxsitecompat.dev/ja/docs/2020/x-content-type-options-nosniff-is-now-enforced-even-if-content-type-is-not-given/) で削除されました。
