---
title: "Атрибут `size`"
description: "Задаёт размеры тегам `<input>` и `<select>`."
authors:
  - inventoris
tags:
  - doka
---

## Кратко

Атрибутом `size` можно задать ширину поля [`<input>`](/html/input/) в символах или количество видимых опций списка в случае [`<select>`](/html/select/).

## Пример

Зададим ширину `<input>` с помощью `size`. Поле ввода растянется так, чтобы в видимую часть поместилось 9 букв моноширинного шрифта.

```html
<label for="city-input">Ваш город</label>
<input id="city-input" size="9" placeholder="не скажу!">
```

<iframe title="Использование атрибута size в input" src="demos/basic_input/" height="250"></iframe>

В примере ниже зададим `size` для `<select>`. Число 3 определит количество видимых параметров списка.

```html
<label for="city-select">Ваш город</label>
<select id="city-select" size="3">
  <option value="novosibirsk">Калининград</option>
  <option value="petrozavodsk">Петрозаводск</option>
  <option value="petrozavodsk">Зеленоград</option>
  <option value="petersburg">Санкт-Петербург</option>
  <option value="samara">Самара</option>
  <option value="perm">Пермь</option>
</select>
```

<iframe title="Использование атрибута size в select" src="demos/basic_select/" height="250"></iframe>

Поскольку `size="3"`, видимая часть списка содержит только 3 города. Чтобы изучить остальные, нужно воспользоваться прокруткой.

## Как понять

В случае `<input>` задать ширину с помощью атрибута `size` можно не для всех типов ввода. Подойдут лишь те, что принимают текстовые данные:

- `type="text"`
- `type="password"`
- `type="email"`
- `type="url"`
- `type="tel"`
- `type="search"`

Если шрифт будет не моноширинный, то выставить ширину `<input>` с помощью атрибута `size` окажется затруднительно.

```css
body {
  font-family: "Roboto", sans-serif;
}
input {
  font-family: inherit;
}
```

```html
<label for="city-input">Ваш город</label>
<input id="city-input" size="10" placeholder="всё ещё не скажу!">
```

<iframe title="Использование атрибута size в input без моноширинного шрифта" src="demos/input_size_without_monospace/" height="250"></iframe>

Как видно из примера, в `<input>` помещается куда больше десяти символов, хотя атрибут `size="10"` задан. Причина в нашем шрифте `Roboto`, — он не моноширинный, а значит в определении ширины поля `<input>` участвовать не будет.

## Подсказки

💡 Если поставить в теге `<select>` атрибут `multiple` и задать `size="1"`, из списка получится обыкновенная «прокрутка».
