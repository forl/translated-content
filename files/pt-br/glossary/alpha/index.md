---
title: Alpha (canal alfa)
slug: Glossary/Alpha
tags:
  - Alfa
  - Canal Alfa
  - Desenhando
  - Glossário
  - Translucidez
  - Translucido
  - Transparente
  - Transparência
  - WebGL
  - WebXR
  - canal
  - cor
  - graficos
  - pixel
translation_of: Glossary/Alpha
original_slug: Glossario/Alpha
---
Cores são representadas no formato digital como uma coleção de números, cada qual sinalizando o nível de força ou intensidade de dado componente da cor. Cada um desses componententes é chamado de **canal**. Num típico arquivo de imagem, o canais de cores descritos devem ser vermelho, verde e azul, que serão usados para definir a cor final. Para representar uma cor que através dela um plano de fundo possa ser visto, um quarto canal é adicionado a ela: o canal alfa. O canal alfa define o nível de opacidade da cor.

Por exemplo, a cor `#8921F2` (também descrita como `rgb(137, 33, 242)` ou` hsl(270, 89%, 54)`) é um belo tom de roxo. Abaixo você pode ver um pequeno retângulo no canto superior esquerdo e outro com a mesma cor, mas tendo um canal alfa defino em 0.5 (50% de opacidade). Os dois retângulos estão desenhados sobre o paragrafo de texto.

![Image showing the effect of an alpha channel on a color.](https://mdn.mozillademos.org/files/17019/alpha-channel-example.png)

Como você pode notar, a cor sem o canal alfa bloqueia completamente o texto ao fundo, enquanto o retângulo com canal alfa definido permite visibilidade através do plano de fundo com cor roxa.

## Saiba mais

### Conhecimento geral

- {{interwiki("wikipedia", "Alpha compositing")}} na Wikipedia
- {{interwiki("wikipedia", "RGBA color model")}} na Wikipedia
- {{interwiki("wikipedia", "Channel (digital image)")}} na Wikipedia

### Referência técnica

- [CSS color](/pt-BR/docs/Web/CSS/CSS_Color)
