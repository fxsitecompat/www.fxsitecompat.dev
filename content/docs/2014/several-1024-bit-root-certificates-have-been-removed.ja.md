---
title: "いくつかの 1024 ビットルート証明書が削除されました"
date: "2014-06-09T02:46:54-04:00"
categories: ["privacy-security"]
tags: []
versions: ["32"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=881553"
      title: "Bug 881553 – Remove or turn off trust bits for 1024-bit root certs after December 31, 2013"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1029561"
      title: "Bug 1029561 – Update Mozilla 32 to use NSS 3.16.3 after July 1st to include root CA updates"
---
継続的な安全性向上の一環として、いくつかの 1024 ビットルート証明書に基づく SSL およびコード署名の信頼が、Firefox やその他の製品で使用されている [Network Security Services (NSS)](https://developer.mozilla.org/docs/Mozilla/Projects/NSS) から削除されました。これには、*AC Raíz Certicámara*、*Entrust.net*、*GTE CyberTrust*、*NetLock*、*TDC Internet*、*ValiCert*、*VeriSign* が含まれます。1024 ビットの証明書はもはや安全と見なされていないことから、Firefox は今後数回のバージョンで [1024 ビットルート証明書をすべて削除します](https://wiki.mozilla.org/CA:MD5and1024)。
