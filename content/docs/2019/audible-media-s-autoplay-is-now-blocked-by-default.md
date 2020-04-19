---
title: "Audible media's autoplay is now blocked by default"
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
Starting with Firefox 66, audible audio and video content can no longer be played automatically both on desktop and mobile, requiring user interaction, usually a click on the play button, to start playing the media. Muted `<video>` and `<audio>` elements that come with the `muted` attribute or the `volume` attribute setting to `0` are still allowed to play. This change aimed at improving Firefox user experience has been tested on the Nightly channel since Firefox 63.

When autoplay is blocked, the `HTMLMediaElement.play` method will return a rejected `Promise`, and an error is logged in the browser's Web Console. The new `allowedToPlay` property also allows to know in advance if calling the `play` method would be blocked. The following example shows how web developers can detect blocking of autoplay:

```js
async function play_video() {
  const $video = document.querySelector('video');

  // Detect in advance
  if ($video.allowedToPlay) {
    $video.play();
    // video started to play
  } else {
    // autoplay will be blocked
    // show a play button
  }

  // or use Promise
  try {
    await $video.play();
    // video started to play
  } catch (ex) {
    // autoplay has been blocked
    // show a play button
  }
}
```

**Update**: The current plan is [turning off blocking autoplay](https://bugzilla.mozilla.org/show_bug.cgi?id=1522923) once in Firefox Beta, then gradually rolling out the feature through the [Shield Program](https://wiki.mozilla.org/Firefox/Shield).

**Update 2**: Autoplay is blocked by default in [Firefox 67](https://bugzilla.mozilla.org/show_bug.cgi?id=1542921) and later.
