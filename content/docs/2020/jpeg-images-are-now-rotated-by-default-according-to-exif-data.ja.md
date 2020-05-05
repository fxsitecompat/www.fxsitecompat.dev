---
title: "JPEG 画像が初期設定で Exif データに従い回転させられるようになりました"
date: "2020-02-17T13:56:00-05:00"
categories: ["css"]
tags: []
releases: ["77"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1566316"
      title: "Bug 1566316 - HTMLImageElement naturalWidth/naturalHeight does not account for image orientation"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1607667"
      title: "Bug 1607667 - [css-images] Consider changing initial value of 'image-orientation' to from-image"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1616169"
      title: "Bug 1616169 - honor intrinsic orientation information in drawImage()"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1616411"
      title: "Bug 1616411 - CSS decorative images should respect EXIF-orientation by default"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1623820"
      title: "Bug 1623820 - make image-orientation initial value be from-image in Nightly only"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1630165"
      title: "Bug 1630165 - drop nightly-only gating of naturalWidth/Height orientation-respecting pref"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1634180"
      title: "Bug 1634180 - Slack shows images at wrong rotation, with the new `image-orientation:from-image` default behavior"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/PDYzBgRz8gk/discussion"
      title: "Intent to ship: a change to the initial value of image-orientation"
aliases:
    - "/ja/docs/2020/initial-value-of-image-orientation-has-been-changed-to-from-image/"
    - "/ja/docs/2020/images-are-now-rotated-by-default-according-to-exif-data/"
---
Firefox 75 で [`image-orientation`](https://developer.mozilla.org/docs/Web/CSS/image-orientation) CSS プロパティの初期値が `none` から `from-image` に変更され、JPEG 画像に保存されている Exif データを向きの調整に用いるようになりました。3 月 17 日公開の [Chrome 81](https://www.chromestatus.com/features/6313474512650240) に初期値を `from-image` としたこのプロパティが実装されるため、何らかの互換性問題があった場合は Firefox 75 がベータ期間を抜ける 4 月 7 日以前に分かるでしょう。もしあなたのサイト上で特定の画像の向きが正しく表示されていないのを発見した場合は、写真編集ソフトでそれらの画像ファイルを修正する必要があります。

[Safari](https://bugs.webkit.org/show_bug.cgi?id=89052) も近い将来このプロパティを実装する予定です。

**更新**: 新型コロナウイルス (COVID-19) の流行により、人々が自宅でより多くの時間をオンラインで過ごすことを余儀なくされています。こうした不安定な時期に Firefox 75 で変更を行うことに関して懸念の声が上がったため、今後のバージョンに延期されました。Nightly チャンネルでは引き続き新たな挙動が有効となります。状況が変わり次第このドキュメントを更新します。

**更新 2**: `image-orientation` プロパティの変更は、Chrome 81 に続く形で、Exif の回転情報を尊重する次にような他の変更とともに Firefox 77 に乗ります。

* `HTMLImageElement` インターフェイス上の `naturalWidth`/`naturalHeight` プロパティ
* `CanvasRenderingContext2D.drawImage` メソッド
* `background-image` や `border-image` などの CSS 装飾用画像

プロパティの変更は *Slack* に影響を与えており、アップロードされた画像が Firefox 77 や Chrome 81 上で正しく回転されません。
