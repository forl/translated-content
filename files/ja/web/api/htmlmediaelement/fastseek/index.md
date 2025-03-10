---
title: HTMLMediaElement.fastSeek()
slug: Web/API/HTMLMediaElement/fastSeek
---

{{APIRef("HTML DOM")}} {{SeeCompatTable}}

**`HTMLMediaElement.fastSeek()`** メソッドは、精度と引き換えにで新しい時間へのメディアを迅速にシークします。

> **Note:** 正確にシークする必要がある場合は、代わりに [`HTMLMediaElement.currentTime`](/ja/docs/Web/API/HTMLMediaElement/currentTime) を設定してください。

## 構文

```js
fastSeek(time)
```

### 引数

- `time`
  - : 倍精度浮動小数点値です。

### 返値

なし ({{jsxref("undefined")}})。

## 例

この例では、 video 要素の 20 秒の位置に素早くシークします。

```js
let myVideo = document.getElementById("myVideoElement");

myVideo.fastSeek(20);
```

## 仕様書

{{Specifications}}

## ブラウザーの互換性

{{Compat}}

## 関連情報

- [HTMLMediaElement.currentTime](/ja/docs/Web/API/HTMLMediaElement/currentTime):
 精度を犠牲にすることなくシークを行う
