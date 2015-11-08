---
title: "セッションストレージのデータサイズが 10 MB に制限されました"
date: "2015-11-08T14:32:00-08:00"
categories: ["dom"]
tags: []
versions: ["45"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1216250": "Bug 1216250 - Limit amount of DOM Storage data stored by Session Restore"
---
[Web Storage API](https://developer.mozilla.org/ja/docs/Web/API/Web_Storage_API)、具体的には [`window.sessionStorage`](https://developer.mozilla.org/ja/docs/Web/API/Window/sessionStorage) プロパティで保存可能なデータの量が、潜在的なブラウザのクラッシュを防ぐため、[オリジン](https://developer.mozilla.org/ja/docs/Glossary/Origin) ごとに 10 MB に制限されました。ローカルに大量のデータを保存する必要があるときは、非同期の [IndexedDB API](https://developer.mozilla.org/ja/docs/Web/API/IndexedDB_API) を代わりに使うことを検討してください。
