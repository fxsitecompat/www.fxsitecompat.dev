---
title: "クロスオリジン `<iframe>` からの位置情報、全画面表示、カメラ、マイク、画面キャプチャリクエストが初期設定で無効化されました"
date: "2020-01-05T20:13:00-05:00"
categories: ["audio-video", "dom", "privacy-security"]
tags: []
versions: ["74"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1483631"
      title: "Bug 1483631 - Restrict nested permission requests (camera/microphone/geolocation/screensharing) with Feature Policy"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1503694"
      title: "Bug 1503694 - FeaturePolicy: Hangouts cannot access microphone from Gmail"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1579373"
      title: "Bug 1579373 - Disabling geolocation permissions by default in cross-origin iframes"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1583142"
      title: "Bug 1583142 - Considering removing third-party \"persistent-storage\" prompting support"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1595720"
      title: "Bug 1595720 - Set Feature Policy default allow list for fullscreen to eself, disable third party by default"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1600883"
      title: "Bug 1600883 - Enable Feature Policy allow attribute and permission delegation by default"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1610572"
      title: "Bug 1610572 - Disable Feature Policy for FF73"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1617219"
      title: "Bug 1617219 - Enable Feature Policy & Permission Delegation for Release 74"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/BdFOMAuCGW8/discussion"
      title: "Intent to prototype: Delegate and restrict permission in third party context"
aliases:
    - "/ja/docs/2012/geolocation-fullscreen-camera-mic-screen-capture-requests-from-cross-origin-iframe-are-now-disabled-by-default/"
---
様々なウェブプラットフォーム機能や API の挙動をウェブ開発者が制御できるようにする [Feature Policy](https://developer.mozilla.org/docs/Web/HTTP/Feature_Policy) への対応が Firefox 74 で追加されました。`<iframe>` 要素上の新しい `allow` 要素を使うことで `<iframe>` 内の機能を制御できますが、ユーザーの混乱を防ぐため、サードパーティに対しては特定の機能が初期設定で無効化されるようになりました。

以下の機能は、その機能が `allow` 属性で明示的に有効化されていない限り、クロスオリジン `<iframe>` 内で使用できなくなりました。

* Geolocation API: [`geolocation`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Feature-Policy/geolocation) ディレクティブ
* Fullscreen API: [`fullscreen`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Feature-Policy/fullscreen) ディレクティブ
* カメラとマイクへのアクセス: [`camera`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Feature-Policy/camera)、[`microphone`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Feature-Policy/microphone) ディレクティブ
* Screen Capture API: [`display-capture`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Feature-Policy/display-capture) ディレクティブ

そのため、例えば、サードパーティ `<iframe>` が Geolocation API を使うことを許可したい場合、以下のように記述する必要があり、そうしないと許可設定リクエストは黙ってブロックされてしまいます。

```html
<iframe src="https://maps.example.com/" allow="geolocation"></iframe>
```

以下の機能は `allow` 属性を使った場合でもクロスオリジン `<iframe>` 内で使用できなくなりました。

* `navigator.storage.persist()` を通じた持続的ストレージ
* Notifications API ([Firefox 70](https://www.fxsitecompat.dev/ja/docs/2019/notification-permission-requests-from-cross-origin-iframe-are-now-disallowed/) 以降)
* Vibration API ([Firefox 72](https://www.fxsitecompat.dev/ja/docs/2019/vibration-api-can-no-longer-be-used-from-cross-origin-iframe/) 以降)

**更新**: この変更は Firefox 73 から 74 へ延期されました。

**更新 2**: *Google Hangouts* がこの変更の影響を受けており、*Gmail* からのマイクアクセスが動作しません。
