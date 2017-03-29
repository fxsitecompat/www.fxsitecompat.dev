---
title: "一部のブラウザー既定フォントが変更されました"
date: "2017-03-29T15:34:00-04:00"
categories: ["misc"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=548311"
      title: "Bug 548311 - Default Japanese font should be Meiryo or Yu Gothic for modern Windows"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=713680"
      title: "Bug 713680 - Use Consolas as the default monospace font on Windows Vista & 7"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1342741"
      title: "Bug 1342741 - Use Menlo as the default monospace font on macOS"
---
Firefox 55 以降、Windows 上では [Consolas](https://en.wikipedia.org/wiki/Consolas)、macOS 上では [Menlo](https://en.wikipedia.org/wiki/Menlo_(typeface)) が、ブラウザーの既定等幅欧文フォントとして使用されます。これまでは、いずれのプラットフォームでも長いこと [Courier New](https://en.wikipedia.org/wiki/Courier_New) が使われてきました。

Windows 上の既定日本語フォントも変更されました。サンセリフ体はＭＳ Ｐゴシックから [メイリオ](https://ja.wikipedia.org/wiki/%E3%83%A1%E3%82%A4%E3%83%AA%E3%82%AA) に、セリフ体はＭＳ Ｐ明朝から游明朝になります。等幅フォントはＭＳ ゴシックのままです。

これにより一部のページで、特にサイズが文字数で指定された `<textarea>` が含まれている場合に、レイアウトが変わる可能性があります。こうした問題はサイズを CSS によってピクセル単位で指定することで防げます。また、例えば [Google Fonts](https://fonts.google.com/) を通じて [ウェブフォント](https://developer.mozilla.org/ja/docs/Learn/CSS/Styling_text/Web_fonts) を使えば、クロスプラットフォーム、クロスブラウザーのデザインを実現できます。
