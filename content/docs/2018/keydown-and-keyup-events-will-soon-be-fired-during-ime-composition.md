---
title: "`keydown` and `keyup` events will soon be fired during IME composition"
date: "2018-05-07T16:20:00-04:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1446401"
      title: "Bug 1446401 - Start to dispatch keydown/keyup events even during composition in Nightly and early Beta"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/oZEz5JH9ZK8/discussion"
      title: "Intent to ship: Start to dispatch \"keydown\" and \"keyup\" events even if composing (only in Nightly and early Beta)"
---
In the near future, to follow the [UI Events spec](https://w3c.github.io/uievents/) and other browsers' behaviour, Firefox will start dispatching the `keydown` and `keyup` events even when compositing with an [Input Method Editor](https://en.wikipedia.org/wiki/Input_method) (IME) is in progress. IME helper applications are used by Chinese, Japanese, Korean and Taiwanese (CJKT) people to input their native multibyte characters in text fields.

In the current release of Firefox, the following events will be fired when you'd like to input "絵" which means picture(s) in Japanese, for example:

1. `keydown { isComposing: false, key: "e", keyCode: 69 }`
1. `compositionstart { data: "" }`
3. `compositionupdate { data: "え" }`
4. `input { isComposing: true }`
5. `compositionupdate { data: "絵" }`
6. `input { isComposing: true }`
7. `compositionend { data: "絵" }`
8. `input { isComposing: false }`
9. `keyup { isComposing: false, key: "Enter", keyCode: 13 }`

In the future releases, this will be:

1. `keydown { isComposing: false, key: "Process", keyCode: 229 }`
2. `compositionstart { data: "" }`
3. `compositionupdate { data: "え" }`
4. `input { isComposing: true }`
5. `keyup { isComposing: true, key: "e", keyCode: 69 }`
6. `keydown { isComposing: true, key: "Process", keyCode: 229 }`
7. `compositionupdate { data: "絵" }`
8. `input { isComposing: true }`
9. `keyup { isComposing: true, key: " ", keyCode: 32 }`
10. `keydown { isComposing: true, key: "Process", keyCode: 229 }`
11. `compositionend { data: "絵" }`
12. `input { isComposing: false }`
13. `keyup { isComposing: false, key: "Enter", keyCode: 13 }`

For comparison, only 4 events will be fired when you type "e" in English:

1. `keydown { isComposing: false, key: "e", keyCode: 69 }`
2. `keypress { isComposing: false }`
3. `input { isComposing: false }`
4. `keyup { isComposing: false, key: "e", keyCode: 69 }`

As you may be aware, the `key` property will be `"Process"` during a composition, and the [`isComposing`](https://developer.mozilla.org/docs/Web/API/KeyboardEvent/isComposing) property will also be `true` between the [`compositionstart`](https://developer.mozilla.org/docs/Web/Events/compositionstart) and [`compositionend`](https://developer.mozilla.org/docs/Web/Events/compositionend) events. That means, if you want to do nothing during a composition, simply check `isComposing` in your `keydown`, `keyup` or `input` event listener like this:

```js
$input.addEventListener('keydown', event => {
  if (event.isComposing) {
    return;
  }
  // Do something
});
```

The new behaviour has already been enabled in the Nightly and early Beta/DevEdition channels as of Firefox 61. Web application developers are encouraged to test with one of the [pre-release builds](https://www.mozilla.org/firefox/channel/desktop/) so the app will continue working as expected for CJKT users. More detailed implementation note can be found in a [newsgroup post](https://groups.google.com/d/topic/mozilla.dev.platform/oZEz5JH9ZK8/discussion) by Mozilla's internationalization engineer.
