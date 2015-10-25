---
title: "Microdata API will be removed by the end of 2015"
date: "2015-10-25T16:27:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=909633": "Bug 909633 - Remove HTML Microdata API"
---
The [Microdata API](http://www.w3.org/TR/microdata/) was implemented with Firefox 16 (and [caused a site compatibility issue](https://www.fxsitecompat.com/en-US/docs/2012/microdata-api-has-added-new-properties-to-elements/)) but later removed from the HTML5 spec, and no other browsers are implementing this API so far. Therefore, Mozilla developers now have a plan to remove the API support from Firefox in Q4 2015. Web developers should avoid using it to retrieve or manipulate microdata including [Schema.org](https://schema.org/).
