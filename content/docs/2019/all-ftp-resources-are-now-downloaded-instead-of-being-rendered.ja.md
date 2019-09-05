---
title: "すべての FTP リソースはレンダリングされずダウンロードされるようになりました"
date: "2019-08-13T17:39:00-04:00"
categories: ["networking"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1560699"
      title: "Bug 1560699 - Consider downloading ftp:// resources rather than rendering them."
---
現在進行中の FTP プロトコル廃止の一環として、Firefox 70 以降、FTP リソースはコンテンツの種類に関わらず、ブラウザー内でレンダリングされる代わりにダウンロードされるようになります。ディレクトリー一覧ページは引き続き生成されますが、今後プレーンテキストの README を含む他のファイルはすべてダウンロード対象となります。[Google Chrome](https://www.chromestatus.com/feature/6199005675520000) は既にバージョン 72 で同様の変更を行っています。FTP サーバーからのファイル配信をやめて HTTPS へ移行することを推奨します。
