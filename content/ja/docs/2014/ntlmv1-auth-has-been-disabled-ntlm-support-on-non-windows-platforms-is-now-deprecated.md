---
title: "NTLMv1 認証が無効化され、Windows 以外のプラットフォームでの NTLM 対応が廃止予定となりました"
date: "2014-03-21T04:50:04-04:00"
categories: ["privacy-security"]
tags: []
versions: "30"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=828183": "Bug 828183 – Firefox enables insecure NTLM (pre-NTLMv2) authentication"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=999306": "Bug 999306 – Allow generic NTLM v1 if pref set"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1023748": "Bug 1023748 – Allow NTLMv1 over SSL/TLS, or intranet access is broken on Firefox 30 for non-Windows platforms"
---
NT LAN Manager バージョン 1 (NTLMv1) ネットワーク認証のセキュリティに問題が見つかっていることから、対応が無効化されました。まだその古いプロトコルを採用している企業や団体は NTLMv2 へアップグレードすべきです。詳しくは、[Honza Bambas のブログ記事](http://www.janbambas.cz/ntlm-v1-and-firefox/) と [Jason Duell による dev-planning メーリングリストへの投稿](https://groups.google.com/d/topic/mozilla.dev.planning/JbrpDmqDLXI) を参照してください。

この変更は SharePoint ベースあるいは IIS 基盤のイントラネットアプリケーションに影響しています。Firefox 30 以降のバージョン何か問題に遭遇した場合は、設定を使い手作業で NTLMv1 を有効化することができます。なお、Windows 以外のプラットフォームでは NTLMv2 に対応していないため、OS X と Linux のユーザは以下のように NTLMv1 を使い続けるためその設定を切り替える必要があります。ただし、Windows 以外のプラットフォームでの NTLM 認証対応は廃止予定とされています。

NTLMv1 の有効化手順: ロケーションバーに `about:config` と入力し、「細心の注意を払って使用する」ボタンをクリック、`network.negotiate-auth.allow-insecure-ntlm-v1` という項目を探し、その上でダブルクリックして値を `true` に変更します。

もうひとつの回避策は、まだ NTLMv1 が有効化されている [Firefox 24 <abbr title="Extended Support Release">ESR</abbr>](http://www.mozilla.jp/business/downloads/) を使うことです。
