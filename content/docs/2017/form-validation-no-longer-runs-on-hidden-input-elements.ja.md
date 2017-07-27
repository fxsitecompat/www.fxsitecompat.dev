---
title: "非表示の `<input>` 要素上ではフォームバリデーションが実行されなくなりました"
date: "2017-03-10T13:42:00-05:00"
categories: ["dom", "html"]
tags: []
versions: ["53"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1319078"
      title: "Bug 1319078 - Form validation should account for the visibility/focusability of the input element"
---
Firefox 53 以降では、Google Chrome のように、[フォームバリデーション](https://developer.mozilla.org/ja/docs/Learn/HTML/Forms/Data_form_validation) 実行時に入力コントロールの可視性が考慮されます。例えば `visibility:hidden` や `display:none` で隠された、フォーカス不能な `<input>` 要素は、入力されている値が実際には無効であっても単純に無視されるようになります。
