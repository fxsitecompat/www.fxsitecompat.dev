---
title: "非標準 `DataTransfer` API が廃止予定となりました"
date: "2018-09-06T05:19:00-04:00"
categories: ["dom"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1453153"
      title: "Bug 1453153 - Add a pref to disable the DataTransfer moz*At APIs for content"
---
[`DataTransfer`](https://developer.mozilla.org/docs/Web/API/DataTransfer) インターフェイス上の非標準メソッド、`mozGetDataAt`、`mozSetDataAt`、`mozClearDataAt`、`mozTypesAt`、および `mozItemCount` プロパティは、Firefox 63 リリース時点で廃止予定とされ、Nightly チャンネル上では無効化されました。Telemetry で一般に使用されていないことが確認されたことから、これらの API は近い将来完全に廃止されます。

`getData`、`setData`、`clearData` メソッド、および `items` プロパティといった標準 API で代用してください。

**更新**: これらのメソッドとプロパティは [Firefox 71](https://www.fxsitecompat.dev/ja/docs/2019/non-standard-datatransfer-apis-have-been-removed/) で削除されました。
