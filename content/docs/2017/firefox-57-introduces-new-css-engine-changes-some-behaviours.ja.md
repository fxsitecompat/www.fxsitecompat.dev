---
title: "Firefox 57 で新しい CSS エンジンが導入され、一部挙動が変わりました"
date: "2017-09-27T03:42:00-04:00"
categories: ["css"]
tags: []
versions: ["57"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1365771"
      title: "Bug 1365771 - stylo: Tracking bug for behavior changes in stylo"
---
2017 年 11 月公開の Firefox 57 には、Quantum CSS あるいは Stylo と呼ばれる [新たな CSS エンジン](https://blog.mozilla.org/blog/2017/09/26/firefox-quantum-beta-developer-edition/) が搭載されます。ウェブページの描画がかつてなく高速になるので、これはエンドユーザーにとってもウェブ開発者にとっても嬉しいニュースです。一方、Style は完全に作り直されたものであるため、Firefox 56 以前で使われていた旧式の CSS エンジンとの挙動の違いが多く見られます。

それら既知の変更点については [MDN 上の開発者リリースノート](https://developer.mozilla.org/ja/Firefox/Releases/57#Quantum_CSS_notes) を参照してください。私たちは Firefox 57 の最終リリース後に見つかったリグレッションを取り上げる予定です。それまでの間、開発者の皆さんには、[Developer Edition](https://www.mozilla.org/firefox/developer/) を使ってサイトやアプリをテストし、[何か問題があれば報告するよう](https://www.fxsitecompat.com/ja/contribute/) 推奨します。
