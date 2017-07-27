---
title: "多くの CSS プロパティから接頭辞が外れました"
date: "2012-10-09T06:00:00-04:00"
categories: ["css"]
tags: []
versions: ["16"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=762302"
      title: "Bug 762302 – [css3-animations] unprefix CSS Animation properties and @keyframes rule"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=762303"
      title: "Bug 762303 – [css3-transitions] unprefix CSS Transition properties"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=745523"
      title: "Bug 745523 – [css3-transforms] Unprefix transforms"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=752187"
      title: "Bug 752187 – Drop prefix for gradients"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=771678"
      title: "Bug 771678 – [css3-values] unprefix calc()"
---
CSS [アニメーション](https://developer.mozilla.org/ja/docs/Web/CSS/CSS_Animations)、[トランジション](https://developer.mozilla.org/ja/docs/Web/CSS/CSS_Transitions)、[トランスフォーム](https://developer.mozilla.org/ja/docs/Web/CSS/CSS_Transforms) の全プロパティが `-moz-` ベンダー接頭辞なしで使用可能となりました。[`@keyframes`](https://developer.mozilla.org/ja/docs/Web/CSS/@keyframes) ルール、[`calc`](https://developer.mozilla.org/ja/docs/Web/CSS/calc) 関数、[グラデーション](https://developer.mozilla.org/ja/docs/Web/CSS/CSS_Images/Using_CSS_gradients) 関数からも接頭辞が外れました。グラデーションについては、接頭辞の有無で [構文が変わっている](https://hacks.mozilla.org/2012/07/aurora-16-is-out/) ため注意が必要です。

接頭辞付きのプロパティや関数を使用する場合は、前方互換性のため、接頭辞なしの形式も必ず併記するようにしましょう。今後、そうした配慮がなされていないスタイルシートは適用されなくなる可能性があります。
