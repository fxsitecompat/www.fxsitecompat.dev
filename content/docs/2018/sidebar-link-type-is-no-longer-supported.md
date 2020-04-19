---
title: "`sidebar` link type is no longer supported"
date: "2018-08-14T23:45:00-04:00"
categories: ["html"]
tags: []
releases: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1452645"
      title: "Bug 1452645 - Remove \"Open in Sidebar\" feature"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/7YXZLzvq6Qg/discussion"
      title: "Intent to Unship: <a rel=\"sidebar\"> support"
---
Firefox 63 has removed the support for the `sidebar` link type that allowed users to bookmark a link that would later be opened in the browser's sidebar. The `window.sidebar.addPanel` method to do the same thing has already been [dropped with Firefox 23](https://www.fxsitecompat.dev/en-CA/docs/2013/ability-to-add-a-sidebar-panel-has-been-dropped/).

`<a rel="sidebar">` will be treated like normal anchor elements from now on. Given that the functionality has been implemented only in Firefox, the compatibility risk should be very low. If your website wants to offer visitors a sidebar panel for easier access, you can [create a browser extension](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/user_interface/Sidebars) instead.
