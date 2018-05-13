---
title: "ドメイン別設定可能セキュリティポリシーは利用できなくなりました"
date: "2014-02-07T11:57:09-05:00"
categories: ["privacy-security"]
tags: []
versions: ["29"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=913734"
      title: "Bug 913734 – Remove domain policy goop from CAPS"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=995943"
      title: "Bug 995943 – local (file://) links don\'t work even when configured for company\'s internal system"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1004260"
      title: "Bug 1004260 – Firefox 29 broke clipboard access; restore the CAPS allowclipboard policy until the Clipboard API allows click-to-copy"
---
Firefox の [設定可能セキュリティポリシー](http://kb.mozillazine.org/Security_Policies) (CAPS) は、ユーザーがブラウザーの高度なセキュリティ設定をカスタマイズして、サイトごとに異なるポリシーを適用可能にする機能です。CAPS にユーザーインターフェイスは用意されていませんが、上級者や法人ユーザーはいくつかの隠し設定を追加することで様々な機能をコントロールできます。CAPS のドメイン別ポリシーは、([NoScript](https://addons.mozilla.org/ja/firefox/addon/noscript/) 拡張機能が UI を提供している) スクリプトブロックを除いて Firefox 29 から削除されました。

法人ユーザーの需要に応えるため、[`localfilelinks` ポリシー](http://kb.mozillazine.org/Links_to_local_pages_do_not_work) は Firefox 30 で復活しました。これは、特に社内アプリケーションにおいて、ウェブページ (`http://` あるいは `https://`) 上にあるローカルファイルシステム (`file:///`) へのリンクを辿れるようにする機能です。差し当たって、[Firefox Beta](https://www.mozilla.org/firefox/channel/) もしくは Mozilla 開発者によって作成された [caps-fileuri](https://addons.mozilla.org/ja/firefox/addon/caps-fileuri/) 拡張機能を使うことで、この制限を回避できます。

[`allowclipboard` ポリシー](http://kb.mozillazine.org/Granting_JavaScript_access_to_the_clipboard) の廃止によって、*CKEditor* など一部のリッチテキストエディターにおいてコピーや貼り付けボタンが動作しなくなっています。標準 [Clipboard API](https://developer.mozilla.org/docs/Web/API/ClipboardEvent) の「クリックでコピー」対応が近い将来実装されます。<kbd>Ctrl</kbd>+<kbd>C</kbd>、<kbd>Ctrl</kbd>+<kbd>V</kbd> といった通常のキーボードショートカットは常に動作するはずです。

**更新**: 「クリックでコピー」対応は [Firefox 41 で実装されました](https://www.fxsitecompat.com/ja/docs/2015/document-execcommand-for-cut-copy-and-paste-no-longer-throws/)。
