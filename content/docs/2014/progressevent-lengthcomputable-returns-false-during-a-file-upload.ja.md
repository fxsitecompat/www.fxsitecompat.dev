---
title: "`ProgressEvent.lengthComputable` がファイルアップロード中に `false` を返します"
date: "2014-02-07T11:57:09-05:00"
categories: ["dom"]
tags: []
versions: ["29"]
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1009640"
      title: "Bug 1009640 – \"Unable to compute\" error on Ebay photo uploader due to XMLHttpRequest lengthComputable == false"
---
[`XMLHttpRequest` `progress` イベントの監視](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/Using_XMLHttpRequest#Monitoring_progress) に使われる [`ProgressEvent.lengthComputable`](https://developer.mozilla.org/docs/Web/API/ProgressEvent.lengthComputable) プロパティが、Firefox 29 でローカルファイルのアップロード中に、本来 `true` を返すべき場合にも `false` を返します。*eBay Picture Uploader* で発見されたこのリグレッションは Firefox 30 で修正されました。
