---
title: ':link'
slug: Web/CSS/:link
tags:
  - Псевдо-классы
translation_of: Web/CSS/:link
---
{{ CSSRef() }}

## Описание

CSS [псевдокласс](/ru/docs/Web/CSS/Псевдо-классы "Pseudo-classes") `:link` позволяет вам выбирать ссылки внутри элементов. Он выберет любую ссылку, которая ещё не была посещена, даже те, которые уже стилизованы, используя селекторы с другими, относящимися к ссылкам, псевдоклассам типа {{ cssxref(":hover") }}, {{ cssxref(":active") }} или {{ cssxref(":visited") }}. Чтобы стилизовать ссылки должным образом, вам нужно вставлять правила `:link` до других, как определено _LVHA-порядком_: `:link` — `:visited` — `:hover` — `:active`. Псевдо-класс {{ cssxref(":focus") }} обычно размещается прямо перед или сразу после `:hover`, в зависимости от ожидаемого эффекта.

> **Примечание:** **Замечание\*\***:\*\* Используйте {{cssxref(":any-link")}} чтобы выбрать ссылку, независимо от того, была она посещена или нет.

## Примеры

```css
a:link {color: slategray;}
.external:link {background-color: lightblue;}
```

## Спецификации

| Спецификация                                                                                 | Статус                                   | Комментарий                                                                       |
| -------------------------------------------------------------------------------------------- | ---------------------------------------- | --------------------------------------------------------------------------------- |
| {{ SpecName('HTML WHATWG', 'scripting.html#selector-link', ':link') }} | {{ Spec2('HTML WHATWG') }}     |                                                                                   |
| {{ SpecName('CSS4 Selectors', '#link', ':link') }}                         | {{ Spec2('CSS4 Selectors') }} | Без изменений.                                                                    |
| {{ SpecName('CSS3 Selectors', '#link', ':link') }}                         | {{ Spec2('CSS3 Selectors') }} | Без изменений                                                                     |
| {{ SpecName('CSS2.1', 'selector.html#link-pseudo-classes', ':link') }} | {{ Spec2('CSS2.1') }}             | Появилось ограничение применять только для элемента {{ HTMLElement("a") }}. |
| {{ SpecName('CSS1', '#anchor-pseudo-classes', ':link') }}                 | {{ Spec2('CSS1') }}                 | Изначальное определение.                                                          |

## Поддержка браузерами

{{Compat}}

## Смотрите также

- {{ cssxref(":visited") }}, {{ cssxref(":hover") }}, {{ cssxref(":active") }}
