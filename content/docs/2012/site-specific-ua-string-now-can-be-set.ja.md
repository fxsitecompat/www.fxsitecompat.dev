---
title: "サイト固有の UA 文字列設定が可能になりました"
date: "2012-12-03T03:50:54-05:00"
categories: ["javascript"]
tags: []
versions: ["17"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=782453"
      title: "Bug 782453 – Add site-specific User Agent infrastructure and use it to fix AOL Mail"
---
米国 *AOL* のウェブメールサービスで、ユーザーエージェント (UA) 文字列に古いビルド日付 (`Gecko/20100101`) が含まれていないと、機能が制限されたベーシック画面に Firefox がフォールバックされてしまうという [問題](https://bugzilla.mozilla.org/show_bug.cgi?id=778408) が報告されています。Mozilla がサイト運営者に連絡を取って修正を依頼しましたが反応がないため、当面の回避策として Firefox 側でサイトごとに UA 文字列を上書きできる仕組みを実装し、それを `aol.com` だけに適用する措置を取りました。具体的には、隠し設定 `general.useragent.override.aol.com` の値を `Gecko/[^ ]*#Gecko/20100101` としています。

[Firefox の UA 文字列](https://developer.mozilla.org/docs/Gecko_user_agent_string_reference) は、[Firefox 4](https://hacks.mozilla.org/2010/09/final-user-agent-string-for-firefox-4/) を皮切りに、時々細かな変更が行われています。ブラウザー判別を行うのであれば、今後も変わる可能性のある UA 文字列を確認するのではなく、特定の機能 (オブジェクトや関数など) が実装されているかどうかを確認する「[機能判別](https://developer.mozilla.org/docs/Browser_Feature_Detection)」の方法を採用することをお勧めします。

<ins datetime="2012-10-12">10/12 更新: *AOL* 側で修正が行われたため、[この隠し設定は削除されました](https://bugzilla.mozilla.org/show_bug.cgi?id=797363)。UA 文字列を上書きする仕組み自体は残っています。</ins>

<ins datetime="2012-11-22">11/22 更新: [一部のオンラインバンク](https://bugzilla.mozilla.org/show_bug.cgi?id=792054) と [ウェブページ作成ツール](https://bugzilla.mozilla.org/show_bug.cgi?id=799502) について、サイト固有の問題を回避するためにこの仕組みが使われています。</ins>
