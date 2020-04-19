---
title: "ウェブページから `view-source:` URL へリンクできなくなりました"
date: "2016-01-30T20:41:00-05:00"
categories: ["privacy-security"]
tags: []
releases: ["47", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1172165"
      title: "Bug 1172165 - Don't let web pages link to view-source: URLs"
---
セキュリティ上の理由から、Firefox は他の特権付き URL と同様に、ウェブページから `view-source:` URL へのリンクをブロックするようになりました。こうした URL は HTML あるいは XML ドキュメントの [ソースを表示](https://developer.mozilla.org/docs/Tools/View_source) するために使われています。Firefox 47 では、`view-source:` URL をクリックするとウェブコンソールに `URI_DANGEROUS_TO_LOAD` の例外が出力されるだけとなります。
