---
title: "間違った Referrer Policy 実装が修正されました"
date: "2015-09-21T21:07:00-04:00"
categories: ["html", "privacy-security"]
tags: []
versions: ["41", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1163743"
      title: "Bug 1163743 - (referrer policy) origin-when-crossorigin should have a hyphen in cross-origin"
---
Firefox は、[`<meta name="referrer">`](https://developer.mozilla.org/docs/Web/HTML/Element/meta#attr-name) と [CSP 1.1 `referrer` ディレクティブ](https://developer.mozilla.org/docs/Web/Security/CSP/CSP_policy_directives#referrer) への対応が Firefox 36 と 37 へそれぞれ追加されて以来、Google Chrome とともに、[リファラポリシー仕様](https://w3c.github.io/webappsec/specs/referrer-policy/) 内に発見された間違ったポリシー値  `origin-when-crossorigin` を実装していました。仕様が更新され、Firefox 41 で正しい値 `origin-when-cross-origin` (追加のハイフンに注意) への対応が追加されました。古い間違った値への対応は将来的に打ち切られます。
