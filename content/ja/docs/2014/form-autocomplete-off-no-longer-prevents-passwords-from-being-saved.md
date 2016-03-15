---
title: "`<form autocomplete=\"off\">` がパスワードの保存を抑止しなくなりました"
date: "2014-03-21T04:50:04-04:00"
categories: ["privacy-security"]
tags: []
versions: ["30"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=956906"
      title: "Bug 956906 – ignore autocomplete=\"off\" when offering to save passwords via the password manager"
---
Firefox は、[`<form>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/form) もしくは [`<input>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/input) 要素に `autocomplete="off"` 属性を設定することで [フォームの自動補完を無効化する](https://developer.mozilla.org/ja/docs/Web/Security/Securing_your_site/Turning_off_form_autocompletion) 手段をページ作者に提供してきました。この機能は今後「本来あるべき」挙動になります。つまり、自動補完はこれまで通り無効化できる一方で、[パスワードマネージャ](https://support.mozilla.org/ja/kb/password-manager-remember-delete-change-passwords) はパスワード保存したいかどうか常にユーザに尋ねるようになります。Internet Explorer と Chrome も同様の変更を行っています。
