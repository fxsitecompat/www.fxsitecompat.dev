---
title: "302 に続く 303、307 リダイレクトが辿られません"
date: "2015-10-20T21:42:00-07:00"
categories: ["networking"]
tags: [""]
versions: ["39"]
statuses: "regressed"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1196882": "Bug 1196882 - Firefox not following 303/7 Status Code after 302"
---
Firefox 39 で標準に準拠しない HTTP レスポンスの扱いが厳密になったため、302 Found に続く 303 See Other あるいは 307 Temporary Redirect ステータスコードによるリダイレクトは辿られなくなりました。しかし、Web 互換性問題により、この新たな挙動は Firefox 41 で取り消されました。
