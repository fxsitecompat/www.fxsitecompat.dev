---
title: "`navigator.mediaDevices` と `navigator.mozGetUserMedia()` が安全でないサイトでは使用できなくなりました"
date: "2019-07-06T20:43:00-04:00"
categories: ["audio-video", "privacy-security"]
tags: []
versions: ["69"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1528031"
      title: "Bug 1528031 - Make navigator.mediaDevices SecureContext (removing it in http)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/vmO0NRM46l8/discussion"
      title: "Intent to deprecate: insecure getUserMedia & enumerateDevices requests"
    - url: "https://blog.mozilla.org/webrtc/camera-microphone-require-https-in-firefox-68/"
      title: "Advancing WebRTC: Camera & microphone require https in Firefox 68."
---
Firefox 69 以降、`navigator.mediaDevices` オブジェクトと非標準の `navigator.mozGetUserMedia` メソッドは HTTPS で配信されたウェブサイトでのみ使用可能となります。安全でないサイトにおいて `navigator.mediaDevices` オブジェクト上の `getUserMedia`、`enumerateDevices` その他のメソッドを呼び出すと、オブジェクトが存在しないため `TypeError` 例外が投げられます。Google Chrome は既に同じ変更をバージョン 74 で行っています。

なお、`getUserMedia` メソッドは [Firefox 68](https://www.fxsitecompat.dev/ja/docs/2019/getusermedia-can-no-longer-be-used-on-insecure-sites/) で既に安全なサイトでのみ使用可能となっています。一方、これらのメソッドは、安全なオリジンとみなされる `http://localhost` では引き続き使用可能となっており、ウェブ開発者はカメラやマイク機能をローカル環境でテストすることが可能です。ただ、本番サイトは常に HTTPS で配信しなければなりません。
