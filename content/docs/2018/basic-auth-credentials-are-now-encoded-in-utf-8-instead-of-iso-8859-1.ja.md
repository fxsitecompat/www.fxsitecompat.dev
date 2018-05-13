---
title: "Basic 認証情報が ISO-8859-1 から UTF-8 によるエンコードに変わりました"
date: "2018-04-06T22:35:00-04:00"
categories: ["networking"]
tags: []
versions: ["59"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1419658"
      title: "Bug 1419658 - Change Basic authentication request header username and password character encoding to UTF-8 (used to be ISO-8859-1)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1449112"
      title: "Bug 1449112 - JBoss authentication issue since FF 59 (problem with accents in authentication window ?) "
---
Firefox は従来、Basic HTTP 認証リクエスト用のユーザー名とパスワードに ISO-8859-1 文字エンコーディングを採用していました。Firefox 59 以降、フランス語のアクセント記号付き文字など非 ASCII 文字が適切にエンコードされるよう、`Authorization` ヘッダーに UTF-8 が採用されます。

あなたのサイトがユーザーの認証情報に英数字や一般的な記号のみを許容している場合、この変更は何ら問題となりません。しかし、非 ASCII のユーザー名やパスワードを受け入れているサイトは ISO-8859-1 と UTF-8 の両方に対応するよう更新する必要があり、さもないとユーザーのログインに問題が生じる可能性があります。

Google Chrome は既に UTF-8 を採用しているため、[RFC 7617](https://tools.ietf.org/html/rfc7617#appendix-B.3) で指摘されているように、人気のアプリケーションフレームワークは `User-Agent` ヘッダーを読み取って、そのブラウザーから送られることが期待される文字エンコーディングを判断しているようです。同じ相互運用性アプローチが Firefox 59 以降にも当てはまるでしょう。Firefox 52 の [延長サポート版](https://www.mozilla.org/firefox/organizations/) (ESR) が 2018 年 8 月まで公開されることを踏まえ、判別コードはブラウザー名だけでなくバージョン番号も確認する必要があります。

今のところ *JBoss Enterprise Application Platform (EAP)* がこの変更による影響を受けることが判明しています。
