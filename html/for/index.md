---
title: "Атрибут `for`"
description: "Устанавливает надёжную связь."
authors:
  - inventoris
related:
  - html/input
  - html/output
  - html/label
tags:
  - doka
---

## Кратко

Атрибут `for` связывает текст в `<label>` либо тэг `<output>` с полем ввода `<input>`.

## Пример

Попробуйте нажать на текст в примере ниже.

```html
<label for="number">Ваше любимое число:</label>
<input id="number">
```

<iframe title="Базовый пример" src="demos/basic/" height="250"></iframe>

Поле `<input>` становится активным, хотя мы его не трогали. Так получается, потому что текст связан с этим полем. Благодаря `for` они словно одно целое 😊

## Как пишется

Связь устанавливается парой атрибутов `for` — `id`, где `for` одного элемента ссылается на `id` другого (или других). Важно помнить, что `for` можно задать только для `<label>` или `<output>`.

```html
<input id="name">
<input id="age">
<output for="name age"></output>
```

## Подсказки

💡 Связь между `<label>` и `<input>` возможно установить без атрибута `for` — достаточно обернуть один другим:

```html
<label>Ваше любимое число: <input id="number"></label>
```
