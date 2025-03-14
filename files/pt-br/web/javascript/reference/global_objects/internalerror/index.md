---
title: InternalError
slug: Web/JavaScript/Reference/Global_Objects/InternalError
translation_of: Web/JavaScript/Reference/Global_Objects/InternalError
---
{{JSRef}} {{non-standard_header}}

O **objeto** **`InternalError` **indica que um erro ocorreu internamente na engine do JavaScript.

Isso ocorre quando algo é muito grande, por exemplo:

- "too many switch cases",
- "too many parentheses in regular expression",
- "array initializer too large",
- "too much recursion".

## Construtor

- [`InternalError()`](/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/InternalError/InternalError)
  - : Cria um um novo objeto `InternalError`.

## Instance properties

- {{jsxref("Error.prototype.message", "InternalError.prototype.message")}}
  - : Error message. Inherited from {{jsxref("Error")}}.
- {{jsxref("Error.prototype.name", "InternalError.prototype.name")}}
  - : Error name. Inherited from {{jsxref("Error")}}.
- {{jsxref("Error.prototype.fileName", "InternalError.prototype.fileName")}}
  - : Path to file that raised this error. Inherited from {{jsxref("Error")}}.
- {{jsxref("Error.prototype.lineNumber", "InternalError.prototype.lineNumber")}}
  - : Line number in file that raised this error. Inherited from {{jsxref("Error")}}.
- {{jsxref("Error.prototype.columnNumber", "InternalError.prototype.columnNumber")}}
  - : Column number in line that raised this error. Inherited from {{jsxref("Error")}}.
- {{jsxref("Error.prototype.stack", "InternalError.prototype.stack")}}
  - : Stack trace. Inherited from {{jsxref("Error")}}.

## Examples

### Too much recursion

This recursive function runs 10 times, as per the exit condition.

```js
function loop(x) {
  if (x >= 10) // "x >= 10" is the exit condition
    return;
  // do stuff
  loop(x + 1); // the recursive call
}
loop(0);
```

Setting this condition to an extremely high value, won't work:

```js example-bad
function loop(x) {
  if (x >= 1000000000000)
    return;
  // do stuff
  loop(x + 1);
}
loop(0);

// InternalError: too much recursion
```

For more information, see [InternalError: too much recursion.](/pt-BR/docs/Web/JavaScript/Reference/Errors/Too_much_recursion)

## Specifications

Not part of any standard.

## Compatibilidade com navegadores

{{Compat("javascript.builtins.InternalError")}}

## See also

- {{jsxref("Error")}}
- [InternalError: too much recursion](/pt-BR/docs/Web/JavaScript/Reference/Errors/Too_much_recursion)
