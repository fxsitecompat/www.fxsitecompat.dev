---
title: "Untrusted `submit` event can no longer trigger form submission"
date: "2019-07-06T23:06:00-04:00"
categories: ["dom"]
tags: []
releases: ["69"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1370630"
      title: "Bug 1370630 - preventDefault() on form.dispatchEvent(new Event('submit'))?"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1556980"
      title: "Bug 1556980 - Impossible to click on the button of jenkins on Firefox Nightly"
---
Previously, Firefox allowed to submit a `<form>` through an untrusted `submit` event generated in a script, not by the user. This Firefox-specific behaviour has been removed with Firefox 69, aiming at improve web interoperability.

```js
// Don't do this
form.dispatchEvent(new Event('submit'));
// Do this
form.submit();
```

However, the form submit button in *YUI 2* is broken due to the change, because it relies on a user-agent detection to call the `submit` method only in Chrome, Safari and Internet Explorer. Mozilla is trying to work around the issue on *Jenkins* that uses YUI, but the chance is, other sites are also affected. If your site still uses the legacy library, you can patch the code in question just like [what the Jenkins team did](https://github.com/jenkinsci/jenkins/pull/3761/files).

**Update**: The change has been backed out due to the compatibility concerns.
