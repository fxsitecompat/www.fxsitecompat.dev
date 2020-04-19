---
title: "スコープ付きスタイルシートへの対応が打ち切られました"
date: "2017-07-13T22:33:00-04:00"
categories: ["css", "html"]
tags: []
releases: ["55", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1291515"
      title: "Bug 1291515 - disable <style scoped> in content documents"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/iBoROFkR9V8/discussion"
      title: "Intent to unship: HTML scoped style sheets (<style scoped>)"
---
Firefox 21 で実装された [HTML スコープ付きスタイルシート](https://developers.google.com/web/updates/2012/03/A-New-Experimental-Feature-style-scoped) は、HTML 仕様から削除されたため、ウェブコンテンツ内では使用できなくなりました。これには、`<style>` HTML 要素上の [`scoped`](https://developer.mozilla.org/docs/Web/HTML/Element/style#attr-scoped) 論理属性、[`scoped`](https://developer.mozilla.org/docs/Web/API/HTMLStyleElement/scoped) DOM プロパティ、[`:scope`](https://developer.mozilla.org/docs/Web/CSS/:scope) CSS 擬似クラスが含まれます。Google Chrome は既に [実装を削除](https://www.chromestatus.com/feature/5374137958662144) しており、現時点で他のどのブラウザーもこの機能に対応していません。
