---
title: "`.scrollIntoView()`"
description: "Прокрутить окно браузера до указанного элемента."
authors:
  - inventoris
contributors:
  - skorobaeus
related:
  - js/dom
  - html/a
  - js/element-scrollto
tags:
  - doka
---

## Кратко

Метод `scrollIntoView()` позволяет программно прокрутить окно до определённого элемента вне зависимости от положения элемента в окне.

## Как пишется

Получаем элемент и накладываем метод `scrollIntoView()`:

```js
const element = document.querySelector('#about')

element.scrollIntoView()
```

🤖 В `scrollIntoView()` можно передать аргумент типа [boolean](/js/boolean/):

- Если указать `true`, то скролл будет перемещён чтобы верхняя граница элемента совпала с верхней границей окна;
- Если указать `false`, то скролл остановится чтобы нижняя граница элемента была вровень с нижней границей окна.

<iframe title="Прокрутка к элементу с помощью логических аргументов" src="demos/basic/" height="450"></iframe>

А ещё в scrollIntoView()` можно передать объект с опциями скролла, где:

- `behavior` для анимации прокрутки. Принимает `smooth`, чтобы было плавно, по умолчанию резко;
- `block` для вертикального выравнивания. Принимает `start`, `center`, `end`, `nearest`;
- `inline` для горизонтального выравнивания, принимает то же, что и `block`.

```js
element.scrollIntoView({behavior: "smooth", block: "center", inline: "center"})
```

<aside>

☎️ В режиме с опциями `scrollIntoView()` не дружит с Safari!

</aside>

## Как это понять

Использовать `scrollIntoView()` полезно в случаях длинных веб-страниц, когда нужно прокрутить страницу к определённым частям, а использования [ссылок с якорями](/html/a/) недостаточно.
