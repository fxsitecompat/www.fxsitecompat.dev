---
title: "`sidebar` リンク形式への対応が廃止されました"
date: "2018-08-14T23:45:00-04:00"
categories: ["html"]
tags: []
releases: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1452645"
      title: "Bug 1452645 - Remove \"Open in Sidebar\" feature"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/7YXZLzvq6Qg/discussion"
      title: "Intent to Unship: <a rel=\"sidebar\"> support"
---
ユーザーが後からブラウザーのサイドバーで開かれるリンクをブックマークできるようにしていた `sidebar` リンクタイプへの対応が Firefox 63 で削除されました。同じことをする `window.sidebar.addPanel` メソッドは既に [Firefox 23 で廃止されています](https://www.fxsitecompat.dev/ja/docs/2013/ability-to-add-a-sidebar-panel-has-been-dropped/)。

今後 `<a rel="sidebar">` は通常のアンカー要素と同様に扱われます。この機能は Firefox にしか実装されていないことから、互換性リスクは非常に低いはずです。あなたのウェブサイトがアクセスを容易にするため訪問者へサイドバーパネルを提供したい場合は、代わりに [ブラウザー拡張機能を作成](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/user_interface/Sidebars) できます。
