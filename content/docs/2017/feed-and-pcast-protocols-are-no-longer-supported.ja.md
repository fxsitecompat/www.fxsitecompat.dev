---
title: "`feed`、`pcast` 両プロトコルへの対応が打ち切られました"
date: "2017-12-26T10:36:00-05:00"
categories: ["misc"]
tags: []
releases: ["59", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1420622"
      title: "Bug 1420622 - Remove Feed and Pcast related protocols"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/abHJ-jaQ5YY/discussion"
      title: "Intent to remove pcast and feed protocols"
---
ウェブフィード処理のための `feed`、`pcast` 両プロトコルへの対応が Firefox 59 で廃止されました。これらは一度も標準化されたことはなく、他のブラウザーにも実装されていません。組み込みのフィードプレビュー機能は今後もこれらのプロトコルのいずれかを伴わない `https` もしくは `http` のフィード URL に対して動作するため、削除に伴うリスクはないはずです。
