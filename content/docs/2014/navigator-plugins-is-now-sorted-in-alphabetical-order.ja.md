---
title: "`navigator.plugins` の並び替えがアルファベット順になりました"
date: "2014-09-01T22:12:15-04:00"
categories: ["dom", "plugins"]
tags: []
versions: ["34"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=793978"
      title: "Bug 793978 – Sort navigator.plugins array to avoid exposing user-identifying plugin file order"
---
[`navigator.plugins`](https://developer.mozilla.org/docs/Web/API/navigator.plugins) 配列はこれまでインストール済みプラグインの最終更新日時によって並べ替えられていました。別々のユーザーがまったく同じ種類のプラグインを持っていた場合でもインストール順はおそらく固有になることから、この実装は、他の特性と組み合わせることで、ユーザー追跡ソフトウェアによってユーザーのフィンガープリンティングに使用される可能性がありました。そうしたフィンガープリンティングのリスクを軽減するため、Firefox 34 以降この配列はプラグイン名のアルファベット順で並び替えられます。
