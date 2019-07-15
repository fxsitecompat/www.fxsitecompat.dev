---
title: "ローカルファイルがそれぞれ別のオリジンを与えられるようになりました"
date: "2019-07-15T12:29:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["68"]
statuses: "affecting"
references:
    - url: "https://www.mozilla.org/en-US/security/advisories/mfsa2019-21/#CVE-2019-11730"
      title: "CVE-2019-11730: Same-origin policy treats all files in a directory as having the same-origin"
---
ローカルに保存された悪質な HTML コンテンツが同じディレクトリにある他のファイルへアクセスするのを防ぐため、Firefox 68 で [同一オリジンポリシー](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy) が強化されました。これはあなた自身のマシン上で直接 `file://` URL を通じてあなたのサイトをテストしていて、例えば別のファイルにスクリプトを含めていたり `<iframe>` を埋め込んでいたりした場合に問題となる可能性があります。

単純な自己完結型の HTML ファイルは今後も表示できるかもしれませんが、構成ファイルを伴ったサイトをテストしたい場合はローカルサーバーを立ち上げることを強くお勧めします。[MAMP](https://www.mamp.info/) や [XAMPP](https://www.apachefriends.org/) といった簡単に使えるツールがありますし、[macOS](https://discussions.apple.com/docs/DOC-3083) には Apache サーバーが内蔵されています。
