---
title: "可聴メディアの自動再生が初期設定でブロックされるようになりました"
date: "2019-02-18T18:55:00-05:00"
categories: ["audio-video", "html"]
tags: []
releases: ["66", "68-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1453862"
      title: "Bug 1453862 - Log to web console when autoplay blocked"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1476853"
      title: "Bug 1476853 - Enable block autoplay in Nightly only"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1478208"
      title: "Bug 1478208 - Expose to web content whether autoplay is blocked"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1487844"
      title: "Bug 1487844 - Flip block autoplay prefs to turn the feature on"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1542921"
      title: "Bug 1542921 - Turn on block autoplay in 67"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/39Q3fW3zl1E/discussion"
      title: "Intent to ship: block audible autoplay media intervention"
---
Firefox 66 以降、デスクトップとモバイルの両方で、可聴な音声・動画コンテンツを自動的に再生することができなくなり、メディアの再生開始にはユーザーインタラクション (通常は再生ボタン上でのクリック) が必要とされるようになりました。`muted` 属性が付いているか `volume` 属性が `0` に設定されている無音の `<video>` や `<audio>` 要素は引き続き再生可能です。Firefox のユーザー体験向上を目的としたこの変更は Firefox 63 以降 Nightly チャンネルでテストされてきました。

自動再生がブロックされた場合、`HTMLMediaElement.play` メソッドは却下された `Promise` を返し、ブラウザーのウェブコンソールにエラーが記録されます。また、新しい `allowedToPlay` を使えば、`play()` メソッドの呼び出しがブロックされるかどうかを事前に知ることが可能です。以下の例はウェブ開発者がどのように自動再生のブロックをどのように判別できるかを示したものです。

```js
async function play_video() {
  const $video = document.querySelector('video');

  // 事前に判別する方法
  if ($video.allowedToPlay) {
    $video.play();
    // 動画の再生は開始されました
  } else {
    // 自動再生はブロックされます
    // 再生ボタンを表示します
  }

  // あるいは Promise を使う方法
  try {
    await $video.play();
    // 動画の再生は開始されました
  } catch (ex) {
    // 自動再生はブロックされました
    // 再生ボタンを表示します
  }
}
```

**更新**: 現在の予定では、Firefox Beta で一度 [自動再生のブロックを無効化](https://bugzilla.mozilla.org/show_bug.cgi?id=1522923) した上で、[Shield Program](https://wiki.mozilla.org/Firefox/Shield) を通じて段階的にこの機能を展開していくことになっています。

**更新 2**: 自動再生は [Firefox 67](https://bugzilla.mozilla.org/show_bug.cgi?id=1542921) 以降初期設定で無効化されています。
