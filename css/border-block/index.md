---
title: "`border-block`"
description: "Когда рамка элемента нужна лишь с двух сторон."
authors:
  - inventoris
related:
  - css/border-width
  - css/border-style
  - css/border-color
tags:
  - doka
---

## Кратко

Свойство `border-block` — это _шорткат_ (короткая запись) для создания видимых границ у двух противоположных сторон блока.

## Пример

Сделаем двустороннюю белую рамку:

```css
div {
  border-block: 20px solid white;
}
```

<iframe title="Двусторонняя рамка сверху и снизу" src="demos/border-up-down/" height="250"></iframe>

## Как понять

С помощью [`border`](/css/border/) можно нарисовать границы блока только со всех сторон. А с помощью `border-block` либо сверху и снизу, либо слева и справа 😎

## Как пишется

`border-block` пишется так же, как и `border`, но сокращает немного другие свойства:

- `border-block-width` — ширину границы;
- `border-block-style` — стиль границы;
- `border-block-color` — цвет границы.

По умолчанию граница создаётся сверху и снизу блока. Но это можно поменять, указав для свойства [`writing-mode`](/css/writing-mode/) значение `vertical-rl`.

```css
div {
  writing-mode: vertical-rl;
}
```

<iframe title="Двусторонняя рамка слева и справа" src="demos/border-left-right/" height="250"></iframe>
