---
title: "ページ遷移時のイベントでダイアログを表示できなくなりました"
date: "2012-12-03T03:50:54-05:00"
categories: ["dom"]
tags: []
versions: ["17"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=391834"
      title: "Bug 391834 – Don\'t allow alert/confirm/prompt in onbeforeunload, onunload and onpagehide"
---
[`beforeunload`](https://developer.mozilla.org/ja/docs/DOM/window.onbeforeunload)、[`unload`](https://developer.mozilla.org/ja/docs/DOM/window.onunload)、[`pagehide`](https://developer.mozilla.org/ja/docs/Using_Firefox_1.5_caching) の各イベントが発生したときに、[`alert`](https://developer.mozilla.org/ja/docs/DOM/window.alert)、[`confirm`](https://developer.mozilla.org/ja/docs/DOM/window.confirm) あるいは [`prompt`](https://developer.mozilla.org/ja/docs/DOM/window.prompt) 関数を使ってダイアログを表示するスクリプトが書かれていても無視されるようになりました。これは、悪意を持ったサイトが、タブを閉じたり、再読み込みしたり、別のページへ移動したりする際に無限ループを発生させ、ブラウザーを終了できなくするといった DoS 攻撃を防ぐための措置です。
