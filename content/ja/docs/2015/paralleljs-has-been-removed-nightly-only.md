---
title: "ParallelJS が削除されました (Nightly のみ)"
date: "2015-01-16T09:37:54-05:00"
categories: ["javascript"]
tags: []
versions: ["37"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1117724"
      title: "Bug 1117724 – [meta] Remove PJS"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1118084"
      title: "Bug 1118084 – Remove self-hosted and user-exposed methods from PJS"
---
[ParallelJS (PJS)](http://wiki.ecmascript.org/doku.php?id=strawman:data_parallelism) の開発が、限られた将来性、関心の薄さ、コードの複雑性といった理由から中止されました。`Array.prototype.mapPar`、`filterPar`、`reducePar` メソッドを含め、Nightly チャンネルのみで有効化されていた試験実装は完全に削除されました。
