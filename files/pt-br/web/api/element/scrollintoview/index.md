---
title: Element.scrollIntoView()
slug: Web/API/Element/scrollIntoView
tags:
  - API
  - CSSOM Views
  - DOM
  - Elemento
  - Experimental
  - Referencia
  - Rolagem
  - View
  - metodo
  - scrollIntoView
translation_of: Web/API/Element/scrollIntoView
---
{{ APIRef("DOM")}}{{SeeCompatTable}}

O método **`Element.scrollIntoView()`** move o elemento ao qual é aplicado para a área visível da janela do navegador.

## Sintaxe

```
element.scrollIntoView(); // Equivalente a element.scrollIntoView(true)
element.scrollIntoView(alignToTop); // Argumentos booleanos
element.scrollIntoView(scrollIntoViewOptions); // argumento Objeto
```

### Parâmetros

- `alignToTop` {{optional_inline}}

  - : É um valor {{jsxref("Boolean")}}:

    - Se `true`, a parte superior do elemento ficará alinhada com o topo da área visível do elemento-pai. Correponde a `scrollIntoViewOptions: {block: "start", inline: "nearest"}`. Este é o valor default.
    - `Se false`, a parte inferior do elemento ficará alinhada com o fundo da área visível do elemento-pai. Corresponde a `scrollIntoViewOptions: {block: "end", inline: "nearest"}`

- `scrollIntoViewOptions` {{optional_inline}}

  - : Um booleano ou um objeto com as seguintes opções:

    ```idl
    {
      behavior: "auto"  | "instant" | "smooth",
      block:    "start" | "center" | "end" | "nearest",
      inline:   "start" | "center" | "end" | "nearest"
    }
    ```

    Caso seja um valor booleano, true corresponde a `{block: "start"}` e false a `{block: "end"}`

    .

## Exemplo

```js
var element = document.getElementById("box");

element.scrollIntoView();
element.scrollIntoView(false);
element.scrollIntoView({block: "end"});
element.scrollIntoView({block: "end", behavior: "smooth"});
```

## Observações

O elemento poderá não ser movido completamento ao topo ou ao fundo dependendo de sua composição com outros elementos.

## Especificações

| Especificação                                                                                                    | Status                           | Comentário        |
| ---------------------------------------------------------------------------------------------------------------- | -------------------------------- | ----------------- |
| {{SpecName("CSSOM View", "#dom-element-scrollintoview", "Element.scrollIntoView()")}} | {{Spec2("CSSOM View")}} | Definição inicial |

## Compatibilidade com navegadores

{{Compat("api.Element.scrollIntoView")}}

## Veja também

- {{domxref("Element.scrollIntoViewIfNeeded()")}}[ ](/pt-BR/docs/Web/API/Element/scrollIntoViewIfNeeded){{non-standard_inline}}
