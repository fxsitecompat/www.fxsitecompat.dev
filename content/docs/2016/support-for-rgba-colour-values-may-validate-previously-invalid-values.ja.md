---
title: "`#RGBA` カラー値への対応により、従来無効だった値が有効になる場合があります"
date: "2016-05-30T09:38:00-04:00"
categories: ["css"]
tags: []
versions: ["49", "52-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=567283"
      title: "Bug 567283 - Add support for 4 and 8 CSS hexcolor values (#RRGGBBAA and #RGBA)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1304810"
      title: "Bug 1304810 - Microsoft Dynamics CRM notes appear to be blank due to #0000 rgba hex parsing"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/00Tq2s58GwA/discussion"
      title: "Intent to implement and ship: #rgba and #rrggbbaa color syntax in CSS"
---
4 桁 (`#RGBA`) および 8 桁 (`#RRGGBBAA`) の 16 進表記による [RGBa カラー値](https://developer.mozilla.org/docs/Web/CSS/color_value#rgba%28%29) への対応が Firefox 49 で追加されました。この変更により、従来無効だった値が有効となり、予期せぬ結果を引き起こす可能性があります。典型的な例は `#0000` で、これは今後 [`transparent`](https://developer.mozilla.org/docs/Web/CSS/color_value#transparent_keyword) と解釈されるようになります。あなたのスタイルシートにそうしたミスがないか再確認した方がいいでしょう。

**更新**: *Microsoft Dynamics CRM 2016* が、一部要素上の文字色に誤って `#0000` を使っているため、影響を受けることが判明しています。
