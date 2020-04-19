---
title: "入れ子になった `<optgroup>` は許容されなくなりました"
date: "2015-10-30T15:02:00-07:00"
categories: ["html", "dom"]
tags: []
releases: ["44", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1214164"
      title: "Bug 1214164 - Only <options> that are children of <select> or children of <optgroup> children of <select> should be honored"
---
HTML5 仕様によれば、入れ子になった [`<optgroup>`](https://developer.mozilla.org/docs/Web/HTML/Element/optgroup) 要素は妥当ではありません。Firefox はこの仕様に従うようになったため、動的に入れ子にされた `<optgroup>` の下に置かれた [`<option>`](https://developer.mozilla.org/docs/Web/HTML/Element/option) 要素は最上位の [`<select>`](https://developer.mozilla.org/docs/Web/HTML/Element/select) 要素のメンバーではなくなります。つまり、その `<option>` は選択できず、`<select>` の `options` DOM プロパティにも現れなくなります。
