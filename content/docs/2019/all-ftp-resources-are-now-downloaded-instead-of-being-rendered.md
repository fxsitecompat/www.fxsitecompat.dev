---
title: "All FTP resources are now downloaded instead of being rendered"
date: "2019-08-13T17:39:00-04:00"
categories: ["networking"]
tags: []
releases: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1560699"
      title: "Bug 1560699 - Consider downloading ftp:// resources rather than rendering them."
---
As part of the ongoing FTP protocol deprecation, Firefox 70 and later will download FTP resources instead of rendering them in the browser regardless of the content type. While directory listing pages are still generated, any other file including a plaintext README will trigger a download from now on. [Google Chrome](https://www.chromestatus.com/feature/6199005675520000) has already made the same change in version 72. It's recommended to stop serving files from a FTP server and migrate to HTTPS.
