---
title: DataView.prototype.setFloat32()
slug: Web/JavaScript/Reference/Global_Objects/DataView/setFloat32
---

{{JSRef}}

**`setFloat32()`** メソッドは、符号付き 32 ビット浮動小数点数 (float) 値を {{jsxref("DataView")}} の指定されたバイト単位のオフセットの位置に格納します。

{{EmbedInteractiveExample("pages/js/dataview-setfloat32.html")}}

## 構文

```
dataview.setFloat32(byteOffset, value [, littleEndian])
```

### 引数

- `byteOffset`
  - : ビューの先頭からのバイト単位のオフセットで、データを格納する位置です。
- `value`
  - : 設定する値です。
- `littleEndian`
  - : {{optional_inline}} 32 ビット浮動小数点数を{{Glossary("Endianness", "リトルエンディアンとビッグエンディアン")}}のどちらの形式で格納するかを表します。 `false` または `undefined` の場合、ビッグエンディアン値が書き込まれます。

### 返値

{{jsxref("undefined")}}。

### 発生するエラー

- {{jsxref("RangeError")}}
  - : `byteOffset` がビューの末尾を超えて格納するように設定されている場合に発生します。

## 例

### setFloat32 メソッドの使用

```js
var buffer = new ArrayBuffer(8);
var dataview = new DataView(buffer);
dataview.setFloat32(1, 3);
dataview.getFloat32(1); // 3
```

## 仕様書

| 仕様書                                                                                                                       |
| ---------------------------------------------------------------------------------------------------------------------------- |
| {{SpecName('ESDraft', '#sec-dataview.prototype.setfloat32', 'DataView.prototype.setFloat32')}} |

## ブラウザーの互換性

{{Compat("javascript.builtins.DataView.setFloat32")}}

## 関連情報

- {{jsxref("DataView")}}
- {{jsxref("ArrayBuffer")}}
