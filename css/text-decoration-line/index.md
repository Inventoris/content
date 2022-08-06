---
title: "`text-decoration-line`"
description: "Украшает текст разными декоративными линиями."
authors:
  - doka-dog
contributors:
  - inventoris
keywords:
  - положение декоративного элемента
tags:
  - doka
  - placeholder
---

## Кратко

Свойство `text-decoration-line` создаёт декоративные линии для текста.

## Пример

Украсим текст разными линиями.

```css
.underline {
  text-decoration-line: underline;
}
.second-1 {
  text-decoration-line: overline underline line-through;
}
.second-2 {
  text-decoration-line: overline underline;
}
.second-3 {
  text-decoration-line: overline;
}
```

<iframe title="Базовый пример" src="demos/basic/" height="300"></iframe>

## Как пишется

Возможные значения:

- `none` — линия не выводится (значение по умолчанию);
- `underline` — линия выводится под текстом, как подчёркивание;
- `overline` — линия выводится над текстом, как надчёркивание;
- `line-through` — линия выводится по центру текста, как перечёркивание.

Из линий можно создавать комбинации, например:

- `underline overline` — линия выводится сверху и снизу текста;
- `underline line-through` — линия выводится снизу и по центру текста;
- `overline line-through` — линия выводится сверху и по центру текста.

Или вовсе добавить сразу три значения:

- `overline underline line-through` — линия выводится везде.

## Подсказки

💡 С помощью свойства `text-decoration-line` можно легко убрать дефолтное подчёркивание ссылки: достаточно указать значение `none`.

```css
a {
  text-decoration-line: none;
}
```

<iframe title="Пример ссылки без подчёркивания" src="demos/link-without-underline/" height="250"></iframe>
