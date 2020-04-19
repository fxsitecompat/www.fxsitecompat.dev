---
title: "日本語の既定フォントが変更されました"
date: "2017-09-20T14:23:00-04:00"
categories: ["misc"]
tags: []
versions: ["57", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=548311"
      title: "Bug 548311 - Default Japanese font should be Meiryo or Yu Gothic for modern Windows"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1351332"
      title: "Bug 1351332 - Needs hack for Meiryo to render italic/oblique style"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1354004"
      title: "Bug 1354004 - Change Japanese default fonts on release build"
aliases:
    - "/ja/docs/2017/some-of-browser-default-fonts-have-been-changed/"
---
Firefox 55 Nightly と Firefox 57 のすべてのチャンネルで Windows 上のブラウザー既定日本語フォントが変更され、ウェブページにモダンな印象が与えられるようになりました。サンセリフ体はＭＳ Ｐゴシックから [メイリオ](https://ja.wikipedia.org/wiki/%E3%83%A1%E3%82%A4%E3%83%AA%E3%82%AA) に、セリフ体はＭＳ Ｐ明朝から游明朝になります。等幅フォントはＭＳ ゴシックのままです。メイリオに斜体はありませんが、Firefox はハックを追加することで、スタイルが適用された場合には斜体となるようにしています。
