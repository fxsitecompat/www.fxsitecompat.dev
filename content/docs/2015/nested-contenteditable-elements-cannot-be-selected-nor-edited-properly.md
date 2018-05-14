---
title: "Nested `contenteditable` elements cannot be selected nor edited properly"
date: "2015-07-07T13:46:34-04:00"
categories: ["html"]
tags: []
versions: ["39"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1181130"
      title: "Bug 1181130 - Broken selection system inside of a nested contenteditable element"
---
The developers of [*CKEditor*](https://ckeditor.com/) have reported that Firefox 39 introduced a regression regarding the text selection and editing on nested [content editable](https://developer.mozilla.org/docs/Web/Guide/HTML/Content_Editable) elements. Editing on such elements is currently difficult because the caret won't appear where clicked, the caret doesn't move with keyboard keys, and non-editable elements are also selected when clicked. Mozilla developers are aware of the issue and working on the solution.

**Update**: According to a comment in the bug, [*MediaWiki VisualEditor*](https://www.mediawiki.org/wiki/VisualEditor)'s table editing functionality is also affected. This bug has already been fixed with Firefox 40 Beta and Firefox 41 Developer Edition.
