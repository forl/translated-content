---
title: bookmarks.get()
slug: Mozilla/Add-ons/WebExtensions/API/bookmarks/get
tags:
  - API
  - Add-ons
  - Bookmraks
  - Extensions
  - Method
  - Non-standard
  - Reference
  - WebExtensions
  - get
translation_of: Mozilla/Add-ons/WebExtensions/API/bookmarks/get
---

{{AddonSidebar()}}

Étant donné l'ID d'un {{WebExtAPIRef("bookmarks.BookmarkTreeNode")}} ou d'un tableau de ces ID, la méthode **`bookmarks.get()`** récupère les nœuds correspondants.

C'est une fonction asynchrone qui renvoie une {{jsxref("promise")}}.

## Syntaxe

```js
var getBookmarks = browser.bookmarks.get(
  idOrIdList                // string or string array
)
```

### Paramètres

- `idOrIdList`
  - : `string` Une {{jsxref("string")}} ou un {{jsxref("array")}} de chaînes spécifiant les ID d'un ou plusieurs objets {{WebExtAPIRef("bookmarks.BookmarkTreeNode", "BookmarkTreeNode")}} à récupérer.

### Valeur retournée

Une {{jsxref("promise")}} qui sera remplie avec un tableau de {{WebExtAPIRef("bookmarks.BookmarkTreeNode", "BookmarkTreeNode")}}, un pour chaque nœud correspondant. Les séparateurs ne sont pas inclus dans les résultats. Si aucun noeud n'a pu être trouvé, la promesse sera rejetée avec un message d'erreur.

## Exemples

Cet exemple essaie d'obtenir le signet dont l'ID est `bookmarkAAAA`. Si aucun signet avec cet ID n'existe, `onRejected` est appelé :

```js
function onFulfilled(bookmarks) {
  console.log(bookmarks);
}

function onRejected(error) {
  console.log(`An error: ${error}`);
}

var gettingBookmarks = browser.bookmarks.get("bookmarkAAAA");
gettingBookmarks.then(onFulfilled, onRejected);
```

{{WebExtExamples}}

## Compatibilité du navigateur

{{Compat("webextensions.api.bookmarks.get")}}

> **Note :**
>
> Cette API est basée sur l'API Chromium [`chrome.bookmarks`](https://developer.chrome.com/extensions/bookmarks). Cette documentation provient de  [`bookmarks.json`](https://chromium.googlesource.com/chromium/src/+/master/chrome/common/extensions/api/bookmarks.json) dans le code Chromium.
>
> Les données de compatibilité relatives à Microsoft Edge sont fournies par Microsoft Corporation et incluses ici sous la licence Creative Commons Attribution 3.0 pour les États-Unis.

<div class="hidden"><pre>// Copyright 2015 The Chromium Authors. All rights reserved.
//
// Redistribution and use in source and binary forms, with or without
// modification, are permitted provided that the following conditions are
// met:
//
//    * Redistributions of source code must retain the above copyright
// notice, this list of conditions and the following disclaimer.
//    * Redistributions in binary form must reproduce the above
// copyright notice, this list of conditions and the following disclaimer
// in the documentation and/or other materials provided with the
// distribution.
//    * Neither the name of Google Inc. nor the names of its
// contributors may be used to endorse or promote products derived from
// this software without specific prior written permission.
//
// THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
// "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
// LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
// A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
// OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
// SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
// LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
// DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
// THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
// (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
// OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
</pre></div>
