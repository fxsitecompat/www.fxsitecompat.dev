---
title: "Loading cross-origin worker no longer throws; worker in sandboxed iframe will fail"
date: "2016-04-02T01:39:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["45"]
statuses: "affected"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1218433"
      title: "Bug 1218433 - Use AsyncOpen2 in dom/workers/ScriptLoader.cpp"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1241888"
      title: "Bug 1241888 - Loading cross-origin worker scripts does not throw a SecurityError"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1260388"
      title: "Bug 1260388 - Web worker fails to load in sandboxed iframe with Firefox 45"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1260961"
      title: "Bug 1260961 - PDF.js doesn't work with cross-origin environment, because worker no longer throws on Firefox 45+ and onerror handler is missing"
---
As part of the HTML5 standard compliance, Firefox 45 has changed the way how to internally load a [Web worker](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API) script. There are 2 backward compatiblity issues you should know.

Previously, Firefox was throwing a `SecurityError` immediately when attempting to load a cross-origin worker script with the [`Worker`](https://developer.mozilla.org/en-US/docs/Web/API/Worker/Worker) constructor. On Firefox 45 and later, a generic `Error` event will be asynchronously fired after a new `Worker` instance is created, according to the latest spec. In order to deal with both cases, you have to use the worker's [`onerror`](https://developer.mozilla.org/en-US/docs/Web/API/AbstractWorker/onerror) handler along with a [`try-catch`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch) statement:

```js
try {
  let worker = new Worker(url);
  worker.addEventListener('error', event => {
    event.preventDefault();
    // Error: Failed to load script (nsresult = 0x805303f4)
    // Handle the error for newer browsers
  });
} catch (ex) {
  // SecurityError
  // Handle the error for older browsers
}
```
Mozilla's [*PDF.js*](https://mozilla.github.io/pdf.js/) library is currently broken in cross-origin environments such as CDNs because it lacks the `onerror` handler for the worker and the fallback function will never get called.

Firefox 45 has also solved an implementation bug where the browser was incorrectly allowing a worker to be loaded in an [`<iframe>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe) with the `sandbox` attribute. Such code now leads to an `Error` as above, because the document in a sandboxed iframe has a unique origin that won't match anything, while worker scripts are required to be [same-origin](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy). The workaround here is adding `allow-same-origin` to the `sandbox` value, though it's not recommended due to the loosened protection.
