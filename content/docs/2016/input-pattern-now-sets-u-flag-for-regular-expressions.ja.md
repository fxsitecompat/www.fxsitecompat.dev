---
title: "`<input pattern>` が正規表現に `u` フラグを設定するようになりました"
date: "2016-04-30T11:13:00-04:00"
categories: ["html"]
tags: []
versions: ["46"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1227906"
      title: "Bug 1227906 - HTML `pattern` attribute should set `u` flag for regular expressions"
    - url: "https://stackoverflow.com/questions/36953775/firefox-error-unable-to-check-input-because-the-pattern-is-not-a-valid-regexp"
      title: "Firefox error: Unable to check input because the pattern is not a valid regexp: invalid identity escape in regular expression"
---
HTML5 で導入された [`<input>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/input) 要素の `pattern` 属性は、ページ作者が定義した正規表現によって入力された値をチェックするために使用されます。Firefox 46 以降、最新の HTML 仕様に従い、ECMAScript 2015 (ES6) で導入された新しい `u` フラグがその正規表現に設定され、一連の Unicode コードポイントとして扱われるようになりました。そのため、例えば `[\@\%]` のようなパターン内の不要あるいは無効なエスケープは「invalid identity escape in regular expression」という `SyntaxError` を投げ、バリデーションは失敗します。
