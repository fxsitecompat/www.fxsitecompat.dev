---
title: "信頼できない `submit` イベントがフォーム送信を実行できなくなりました"
date: "2019-07-06T23:06:00-04:00"
categories: ["dom"]
tags: []
versions: ["69"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1370630"
      title: "Bug 1370630 - preventDefault() on form.dispatchEvent(new Event('submit'))?"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1556980"
      title: "Bug 1556980 - Impossible to click on the button of jenkins on Firefox Nightly"
---
これまで Firefox は、ユーザーではなくスクリプトによって生成された信頼できない `submit` イベントを通じて `<form>` を送信することを許容していました。この Firefox 固有の挙動は、ウェブの相互運用性向上を目的として、Firefox 68 で削除されました。

```js
// 非推奨
form.dispatchEvent(new Event('submit'));
// 推奨
form.submit();
```

しかし、この変更により、ユーザーエージェント判別に依存して Chrome、Safari、Internet Explorer のみで `submit` メソッドを呼び出している *YUI 2* のフォーム送信ボタンが動かなくなっています。Mozilla は YUI を使用している *Jenkins* 上でこの問題を回避しようと試みていますが、他のサイトも影響を受ける可能性が大いにあります。あなたのサイトがまだこの旧式ライブラリを使用している場合は、[Jenkins チームがやったように](https://github.com/jenkinsci/jenkins/pull/3761/files) 当該コードにパッチを当てることができます。

**更新**: この変更は互換性に関する懸念によりバックアウトされました。
