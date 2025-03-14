---
title: suffix
slug: Web/CSS/@counter-style/suffix
tags:
  - CSS
  - Descripteur
  - Reference
translation_of: Web/CSS/@counter-style/suffix
---

{{CSSRef}}

Le descripteur **`suffix`**, utilisé avec la règle @ {{cssxref("@counter-style")}}, afin de définir un symbole qui pourra être utilisé comme suffixe pour la représentation du marqueur. Le symbole en question pourra être une chaîne de caractères, une image ou un identifiant CSS. La valeur par défaut de ce descripteur sera `"\2E\20"` (un point « . » suivi par un espace).

## Syntaxe

```css
/* Une valeur de type <symbol> */
suffix: "";
suffix: ") ";
```

### Valeur

- `<symbol>`
  - : Un symbole qui sera ajouté comme suffixe à la représentation du marqueur. Cette valeur peut être une valeur de type {{cssxref("&lt;string&gt;")}}, {{cssxref("&lt;image&gt;")}} ou {{cssxref("&lt;custom-ident&gt;")}}.

### Syntaxe formelle

{{csssyntax}}

## Exemples

### CSS

```css
@counter-style options {
  system: fixed;
  symbols: A B C D;
  suffix: ") ";
}

.exemple {
  list-style: options;
}
```

### HTML

```html
<ul class="exemple">
  <li>Un</li>
  <li>Deux</li>
  <li>Trois</li>
  <li>Autre</li>
</ul>
```

### Résultat

{{EmbedLiveSample('Exemples')}}

## Spécifications

| Spécification                                                                                            | État                                         | Commentaires         |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------- | -------------------- |
| {{SpecName('CSS3 Counter Styles', '#descdef-counter-style-suffix', 'suffix')}} | {{Spec2('CSS3 Counter Styles')}} | Définition initiale. |

{{cssinfo}}

## Compatibilité des navigateurs

{{Compat("css.at-rules.counter-style.suffix")}}

## Voir aussi

- {{cssxref("list-style")}},
- {{cssxref("list-style-image")}},
- {{cssxref("list-style-position")}},
- {{cssxref("symbols", "symbols()")}}, la notation fonctionnelle utilisée pour créer des styles de compteur anonymes.
