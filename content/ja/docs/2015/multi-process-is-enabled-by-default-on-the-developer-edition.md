---
title: "Developer Edition でマルチプロセスが初期設定で有効となりました"
date: "2015-08-05T00:48:18-04:00"
categories: ["misc"]
tags: []
versions: "43"
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1188605": "Bug 1188605 - Turn e10s on by default for 42/aurora"
---
Firefox 42 以降、[Electrolysis](https://wiki.mozilla.org/Electrolysis) (e10s) と呼ばれる新しいマルチプロセスモードが、Firefox Nightly に加えて [Firefox Developer Edition](https://developer.mozilla.org/ja/Firefox/Developer_Edition) (Aurora) でも初期設定で有効となります。e10s は Firefox の中核部に多くの抜本的な変更を必要とすることから、多くの Web 機能がまだ正しく動作していません。未修正の問題については [Bug 516752 の依存ツリー](https://bugzilla.mozilla.org/showdependencytree.cgi?id=516752&maxdepth=1&hide_resolved=1) を参照し、もし何か他の問題に遭遇した場合はバグを報告してください。なお、[Bug 1188818](https://bugzilla.mozilla.org/show_bug.cgi?id=1188818) のように、一部の問題は e10s が「無効」の場合に発生する可能性があります。

**更新**: この変更は「非 e10s テストが十分に揃っていない」ため [Firefox 43 に延期されました](https://bugzilla.mozilla.org/show_bug.cgi?id=1203184)。
