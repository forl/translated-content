---
title: extension.isAllowedFileSchemeAccess()
slug: Mozilla/Add-ons/WebExtensions/API/extension/isAllowedFileSchemeAccess
tags:
  - API
  - Add-ons
  - Extension
  - Extensions
  - Méthode
  - Non-standard
  - Reference
  - WebExtensions
  - isAllowedFileSchemeAccess
translation_of: Mozilla/Add-ons/WebExtensions/API/extension/isAllowedFileSchemeAccess
---

{{AddonSidebar()}}Renvoie `true` si l'extension peut accéder au schéma "file://", sinon `false`.

C'est une fonction asynchrone qui renvoie une [`Promise`](/fr/docs/Web/JavaScript/Reference/Objets_globaux/Promise).

## Syntaxe

```js
var isAllowed = browser.extension.isAllowedFileSchemeAccess()
```

### Paramètres

None.

### Valeur retournée

Une [`Promise`](/fr/docs/Web/JavaScript/Reference/Objets_globaux/Promise) qui sera remplie avec un booléen : `true` si l'extension est autorisée à accéder aux URLs "file://", sinon `false`.

Firefox retournera toujours `false`.

## Compatibilité du navigateur

{{Compat("webextensions.api.extension.isAllowedFileSchemeAccess")}}

## Exemples

```js
function logIsAllowed(answer) {
  console.log(`Is allowed: ${answer}`);
}

var isAllowed = browser.extension.isAllowedFileSchemeAccess();
isAllowed.then(logIsAllowed);
```

{{WebExtExamples}}

> **Note :**
>
> Cette API est basée sur l'API Chromium [`chrome.extension`](https://developer.chrome.com/extensions/extension). Cette documentation est dérivée de [`extension.json`](https://chromium.googlesource.com/chromium/src/+/master/chrome/common/extensions/api/extension.json) dans le code Chromium.
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
