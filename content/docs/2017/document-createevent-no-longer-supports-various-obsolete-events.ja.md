---
title: "`document.createEvent()` が様々な古いイベントに非対応となりました"
date: "2017-06-07T08:07:00-04:00"
categories: ["dom"]
tags: []
versions: ["55", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1251198"
      title: "Bug 1251198 - Align document.createEvent() supported events with spec"
---
様々な古い非標準イベントへの対応が [`document.createEvent`](https://developer.mozilla.org/docs/Web/API/Document/createEvent) メソッドから削除されました。これには、`CommandEvent`、`CommandEvents`、`DataContainerEvent`、`DataContainerEvents`、`DragEvents`、`NotifyPaintEvent`、`PageTransition`、`PopUpEvents`、`SimpleGestureEvent`、`SVGEvent`、`TextEvents`、`TimeEvents` が含まれます。
