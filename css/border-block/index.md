---
title: "`border-block`"
description: "Создаёт рамки элементу по направлению текста."
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

Свойство `border-block` — это шорткат для создания видимых границ блока по направлению текста.

## Пример

Сделаем двустороннюю белую рамку для текстового блока:

```css
div {
  border-block: 5px solid white;
}
```

<iframe title="Двусторонняя рамка по направлению текста" src="demos/border-block-basic/" height="250"></iframe>

## Как понять

С помощью [`border`](/css/border/) можно нарисовать границы блока только со всех четырёх сторон и не важно, куда направлен текст. А с помощью `border-block` граница отрисуется только с двух сторон и строго по направлению текста 😎

Эту особенность легко увидеть, если поменять для текстового блока направление письма на вертикальное:

```css
div {
  writing-mode: vertical-rl;
}
```

<iframe title="Двусторонняя рамка при вертикальном написании" src="demos/border-block-reverse/" height="250"></iframe>

Поскольку `border-block` связан с направлением текста, границы изменились, и теперь они слева и справа.

## Как пишется

`border-block` пишется так же, как и `border`, а ещё сокращает такие же свойства. Отличие лишь в том, что `border` в записи заменяется на `border-block`:

- `border-block-width` — ширина границы;
- `border-block-style` — стиль границы;
- `border-block-color` — цвет границы.


## Подсказки

💡 Когда нужно, чтобы видимые границы блока разместились перпендикулярно направлению текста, используйте свойство `border-inline` — оно обратное по отношению к `border-block`.

```css
div {
  border-inline: 5px solid white;
}
```

<iframe title="Двусторонняя рамка против направления текста" src="demos/border-inline/" height="250"></iframe>
