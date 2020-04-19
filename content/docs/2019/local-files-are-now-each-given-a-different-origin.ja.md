---
title: "ローカルファイルがそれぞれ別のオリジンを与えられるようになりました"
date: "2019-07-15T12:29:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["68", "68-esr"]
statuses: "affecting"
references:
    - url: "https://www.mozilla.org/en-US/security/advisories/mfsa2019-21/#CVE-2019-11730"
      title: "CVE-2019-11730: Same-origin policy treats all files in a directory as having the same-origin"
---
ローカルに保存された悪質な HTML コンテンツが同じディレクトリーにある他のファイルへアクセスするのを防ぐため、Firefox 68 で [同一オリジンポリシー](https://developer.mozilla.org/docs/Web/Security/Same-origin_policy) が強化されました。これはあなた自身のマシン上で直接 `file://` URL を通じてあなたのサイトをテストしていて、例えば別のファイルにスクリプトを含めていたり `<iframe>` を埋め込んでいたりした場合に問題となる可能性があります。

単純な自己完結型の HTML ファイルは今後も表示できるかもしれませんが、構成ファイルを伴ったサイトをテストしたい場合はローカルサーバーを立ち上げることを強くお勧めします。[MAMP](https://www.mamp.info/) や [XAMPP](https://www.apachefriends.org/) といった簡単に使えるツールがありますし、[macOS](https://discussions.apple.com/docs/DOC-3083) には Apache サーバーが内蔵されています。

**更新**: この変更は、ウェブフォント、Worker、XSLT など、他の様々なものにも影響を与えています。[Bug 1566172](https://bugzilla.mozilla.org/show_bug.cgi?id=1566172) にこうした事例のリストがあります。
