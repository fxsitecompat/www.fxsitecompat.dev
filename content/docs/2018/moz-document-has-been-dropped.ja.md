---
title: "`@-moz-document` 対応が打ち切られました"
date: "2018-03-18T16:09:00-04:00"
categories: ["css", "privacy-security"]
tags: []
versions: ["61"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1035091"
      title: "Bug 1035091 - limit @-moz-document to user and UA sheets (Makes it useless for exfiltration in CSS-injection attacks)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1422245"
      title: "Bug 1422245 - Toggle the pref to disable @-moz-document in content pages on release"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1426068"
      title: "Bug 1426068 - Disabling @-moz-document results in users being unable to enter line-breaks into YouTube comments"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/RysotXvooV0/discussion"
      title: "Intent to unship: @-moz-document from content pages."
aliases:
    - "/ja/docs/2015/moz-document-support-has-been-dropped/"
    - "/ja/docs/2015/moz-document-support-will-be-dropped/"
---
[`@-moz-document`](https://developer.mozilla.org/ja/docs/Web/CSS/@document) ルールがウェブコンテンツから使用できなくなりました。これは、第三者サイトの URL に含まれる機密データを盗み出す目的で、攻撃者による CSS インジェクションに悪用される恐れがあったためです。Firefox ユーザーは引き続きユーザースタイルシート内でこのルールを使い、ブラウジング体験をパーソナライズすることが可能です。

この @ 規則対応は Firefox 59 の時点で既に Nightly と早期 Beta/DevEdition から削除されており、Firefox 61 ですべてのチャンネルから完全に削除されました。

*YouTube* のコメントがこの変更によって動作していないことが判明していましたが、Google によって互換性問題は修正されました。*Air Canada* と *Telegram* のウェブサイトにおける不具合は Firefox 側で解決が行われました。そうした状況から考えると、まだ他のサイトが影響を受ける可能性があります。
