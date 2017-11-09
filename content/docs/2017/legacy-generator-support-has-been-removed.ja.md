---
title: "旧式ジェネレーター対応が廃止されました"
date: "2017-11-08T15:15:00-05:00"
categories: ["javascript"]
tags: []
versions: ["58"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083476"
      title: "Bug 1083476 - Add console warnings for JS1.7 legacy generators"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083482"
      title: "Bug 1083482 - Remove SpiderMonkey support for JS1.7 legacy generators"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1119777"
      title: "Bug 1119777 - Remove non-standard Function.prototype.isGenerator"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1413867"
      title: "Bug 1413867 - Remove StopIteration"
aliases:
    - "/ja/docs/2015/iterator-method-will-be-removed/"
    - "/ja/docs/2015/legacy-iterator-and-generator-support-will-be-removed/"
---
[JavaScript 1.7](https://developer.mozilla.org/ja/docs/Web/JavaScript/New_in_JavaScript/1.7) で導入され、Firefox 57 以降廃止予定となっていた非標準のジェネレーター対応は Firefox 58 で削除されました。これには、[`StopIteration`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/StopIteration) オブジェクト、[`Function.prototype.isGenerator`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Function/isGenerator) メソッド、[旧式ジェネレーター関数命令文](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/Legacy_generator_function)、[旧式ジェネレーター関数式](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/Legacy_generator_function)、[旧式ジェネレーターオブジェクト](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Generator#Legacy_generator_objects) が含まれます。

旧式イテレータープロトコル対応は [Firefox 57](https://www.fxsitecompat.com/ja/docs/2017/legacy-iterator-protocol-has-been-removed/) で既に削除されています。それぞれの置き換え例に関しては [標準のジェネレーターとイテレーター](https://developer.mozilla.org/ja/docs/Web/JavaScript/Guide/Iterators_and_Generators) を参照してください。
