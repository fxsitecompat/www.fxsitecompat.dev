---
title: "`Accept-Language` ヘッダー内の言語名が常に正規化されるようになりました"
date: "2015-10-27T00:50:00-07:00"
categories: ["networking", "privacy-security"]
tags: []
releases: ["36", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1054739"
      title: "Bug 1054739 - Reduce HTTP Accept-Language Entropy"
---
これまで、ユーザーがブラウザーの設定ページを通じて自分の優先言語を変更した場合、HTTP `Accept-Language` リクエストヘッダー内の言語名が `en-US` から `en-us` のように小文字に変わっていました。単にそれらの言語名が正規化されていないというだけでなく、そのような挙動はブラウザーのフィンガープリンティングの可能性を高めるものであったため、この問題は Firefox 36 で修正されました。
