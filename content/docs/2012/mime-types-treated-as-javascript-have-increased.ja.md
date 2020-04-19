---
title: "JavaScript として扱われる MIME タイプが増えました"
date: "2012-12-03T03:50:54-05:00"
categories: ["javascript"]
tags: []
releases: ["17"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=672814"
      title: "Bug 672814 – Increase the set of script @type values that nsScriptLoader treats as JavaScript"
---
Firefox では、`text/javascript`、`text/ecmascript`、`application/javascript`、`application/ecmascript`、`application/x-javascript` 以外の MIME タイプが設定されたスクリプトは JavaScript と見なされていませんでした。例えば `<script type="text/jscript"> ... </script>` のようなコードは、Firefox の以前のバージョンでは動作しません。Firefox 17 では、HTML5 草案に合わせ、`text/jscript` を含む様々な MIME タイプに対応しました。これにより、従来 Firefox で実行されなかったスクリプトが実行されるようになり、思わぬ不具合を生む可能性があるかもしれません。
