---
title: "`window.sidebar` と `window.external.AddSearchProvider()` が廃止予定となりました"
date: "2018-10-31T22:32:00-04:00"
categories: ["dom"]
tags: []
versions: ["65"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1503551"
      title: "Bug 1503551 - Make window.external.AddSearchProvider a dummy function"
---
`window.external` のエイリアスとなっている非標準で Netscape 由来の [`window.sidebar`](https://developer.mozilla.org/docs/Web/API/window.sidebar) オブジェクトは、正式に廃止予定となり、[将来的に削除されます](https://www.fxsitecompat.com/ja/docs/2015/window-sidebar-will-be-removed/)。このオブジェクトは Firefox 65 以降 Nightly チャンネルでは使用できなくなりました。ウェブ開発者の皆さんはこれをブラウザー判別に使うのをやめてください。

IE 由来の `window.external` オブジェクトは残されますが、最新の HTML 仕様に従い、その上で提供されている `AddSearchProvider`、`IsSearchProviderInstalled` 両メソッドは no-op (何もしない) となり、単に `undefined` を返すようになります。この変更も Firefox 65 Nightly で行われました。`AddSearchProvider` は OpenSearch プラグインをブラウザーへ追加するために使うことができましたが、`IsSearchProviderInstalled` は Firefox では常に `0` を返していました。

`<link rel="search">` を通じた [検索プラグインの自動検出](https://developer.mozilla.org/docs/Web/OpenSearch#Autodiscovery_of_search_plugins) を廃止する予定はなく、これがウェブサイト上で OpenSearch プラグインを提供するための推奨方法です。
