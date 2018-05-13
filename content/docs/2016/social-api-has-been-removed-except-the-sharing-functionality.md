---
title: "Social API has been removed except the sharing functionality"
date: "2016-08-15T14:58:00-04:00"
categories: ["misc"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1289549"
      title: "Bug 1289549 - SocialAPI deprecation"
---
The most part of the non-standard [Social API](https://developer.mozilla.org/docs/Mozilla/Projects/Social_API) has been removed except for the [page sharing functionality](https://developer.mozilla.org/docs/Mozilla/Projects/Social_API/Share) implemented by [various service providers](https://activations.cdn.mozilla.net/en-US/). The Firefox-specific API was [introduced back in 2012](https://blog.mozilla.org/labs/2012/03/experimenting-with-social-features-in-firefox/) to integrate social features like [Facebook Messenger](https://blog.mozilla.org/futurereleases/2012/10/22/help-us-test-the-social-api-with-facebook-messenger-for-firefox/) into the browser without having to relying on add-ons. However, it has not been actively promoted nor widely used, hence the deprecation. Mozilla has already notified a small number of affected providers offering a sidebar.
