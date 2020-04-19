---
title: "非標準 `DataTransfer` API が削除されました"
date: "2019-09-05T18:13:00-04:00"
categories: ["dom"]
tags: []
releases: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1345192"
      title: "Bug 1345192 - Consider removing gecko-only DataTransfer APIs"
---
[Firefox 63](https://www.fxsitecompat.dev/ja/docs/2018/non-standard-datatransfer-apis-have-been-deprecated/) 以降廃止予定となっていた、[`DataTransfer`](https://developer.mozilla.org/docs/Web/API/DataTransfer) インターフェイス上の非標準メソッド `mozGetDataAt`、`mozSetDataAt`、`mozClearDataAt`、`mozTypesAt` および `mozItemCount` プロパティが、Firefox 71 で削除されました。標準の `getData`、`setData`、`clearData` メソッドおよび `items` プロパティを代わりに使用してください。
