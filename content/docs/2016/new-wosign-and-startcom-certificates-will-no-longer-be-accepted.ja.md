---
title: "WoSign と StartCom の新規証明書は受け入れられなくなります"
date: "2016-10-25T09:17:00-04:00"
categories: ["privacy-security"]
tags: []
releases: ["51", "52-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1309707"
      title: "Bug 1309707 - Distrust new certs chaining up to current WoSign/StartCom roots"
    - url: "https://blog.mozilla.org/security/2016/10/24/distrusting-new-wosign-and-startcom-certificates/"
      title: "Mozilla Security Blog: Distrusting New WoSign and StartCom Certificates"
---
Mozilla は、入念な調査の結果、*WoSign* と *StartCom* という 2 つの認証局 (CA) における様々な「技術上および経営上の問題」を発見し、2016 年 10 月 21 日以降に両社から発行された新規証明書を信頼しないことを決定しました。既存顧客への影響を避けるため古い証明書は引き続き受け入れられますが、影響を受けたルート証明書は将来的に Firefox から削除されます。本件に関する詳細と Mozilla の措置については [この Security Blog の記事](https://blog.mozilla.org/security/2016/10/24/distrusting-new-wosign-and-startcom-certificates/) を参照してください。
