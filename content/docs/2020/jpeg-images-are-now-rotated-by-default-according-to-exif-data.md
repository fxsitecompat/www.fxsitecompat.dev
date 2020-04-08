---
title: "JPEG images are now rotated by default according to Exif data"
date: "2020-02-17T13:56:00-05:00"
categories: ["css"]
tags: []
versions: ["75"]
statuses: "postponed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1607667"
      title: "Bug 1607667 - [css-images] Consider changing initial value of 'image-orientation' to from-image"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1623820"
      title: "Bug 1623820 - make image-orientation initial value be from-image in Nightly only"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/PDYzBgRz8gk/discussion"
      title: "Intent to ship: a change to the initial value of image-orientation"
aliases:
    - "/en-CA/docs/2020/initial-value-of-image-orientation-has-been-changed-to-from-image/"
    - "/en-CA/docs/2020/images-are-now-rotated-by-default-according-to-exif-data/"
---
Firefox 75 has changed the initial value of the [`image-orientation`](https://developer.mozilla.org/docs/Web/CSS/image-orientation) CSS property from `none` to `from-image`, which uses Exif data stored in JPEG images for rotation. [Chrome 81](https://www.chromestatus.com/features/6313474512650240) is shipping the property on March 17 with defaulting to `from-image`, so any compatibility issue could be noticed before Firefox 75 goes out of beta on April 7. If you find certain pictures on your site not rotating properly, you need to modify these image files with a photo editor.

[Safari](https://bugs.webkit.org/show_bug.cgi?id=89052) is also shipping the property in the near future.

**Update**: The novel coronavirus (COVID-19) outbreak is forcing people to spend more time online at home. Due to concerns around making the change with Firefox 75 during such an uncertain time, it has been postponed to a future release. The new behaviour remains enabled on the Nightly channel. We’ll update this note when the situation has changed.
