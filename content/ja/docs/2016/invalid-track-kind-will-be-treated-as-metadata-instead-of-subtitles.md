---
title: "不正な `<track kind>` は `subtitles` ではなく `metadata` として扱われます"
date: "2016-05-10T12:24:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1269712"
      title: "Bug 1269712 - A <track kind=invalid> should behave like metadata, not subtitles"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/42-W463M4Ig/discussion"
      title: "Intent to ship: invalid <track kind> values behave like \"metadata\", not \"subtitles\""
---
従来、[`<track>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/track) 要素上の `kind` 属性に指定された不正な値は、既定値の `subtitles` として扱われていました。将来後方互換性を損なうことなく新しい種類を導入できるよう、そうした不正な値はユーザが誤って見ることのない `metadata` と同様の挙動になりました。Opera の調査によれば、わずかに 0.001% のページがこの変更による影響を受けます。
