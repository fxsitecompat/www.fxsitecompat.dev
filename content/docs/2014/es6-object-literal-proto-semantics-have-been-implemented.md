---
title: "ES6 object-literal `__proto__` semantics have been implemented"
date: "2014-10-17T22:50:44-04:00"
categories: ["javascript"]
tags: []
versions: ["35", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1061853"
      title: "Bug 1061853 – Implement ES6 object-literal __proto__ restrictions/semantics"
---
ECMAScript 6 semantics and restrictions for [prototype mutations in object literals](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Object_initializer#Prototype_mutation) have been implemented. Now only a single prototype mutation is allowed in an object literal with a [`__proto__`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/proto); multiple mutation raises a [`SyntaxError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError). Also, method members like `__proto__() {}` will not override the prototype anymore.
