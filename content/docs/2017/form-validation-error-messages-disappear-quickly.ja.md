---
title: "フォームバリデーションエラーメッセージが即座に消えてしまいます"
date: "2017-04-24T00:42:00-04:00"
categories: ["dom", "html"]
tags: []
releases: ["53"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1358487"
      title: "Bug 1358487 - Native form validation error messages do not appear"
---
ブラウザーのネイティブ [フォームデータバリデーション](https://developer.mozilla.org/docs/Learn/HTML/Forms/Form_validation) エラーメッセージが一瞬のうちに消えてしまい、それによってユーザーが入力内容の間違いを把握しづらくなるというリグレッションが Firefox 53 で発生しました。この問題は Firefox 54 Beta では修正済みです。Firefox 53 のマイナーアップデートがもし公開された場合は、それにもパッチが含まれる可能性があります。

**更新**: この問題は Firefox 53.0.2 で修正されました。
