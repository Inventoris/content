🛠 Свойство `border-block` открывает пространство для творчества. Его можно сочетать с обычным `border`, тогда каждая граница рисуется отдельно друг от друга, образуя интересные фигуры:

```css
div {
  background-color: #F498AD;
  border: 70px solid #2E9AFF;
  border-block: 70px solid white;
}
```

<iframe title="Пирамида из рамок" src="../demos/border-pyramid/" height="250"></iframe>

🛠 Если изменять свойства `border`, то и `border-block` начнёт меняться, — они связаны. Поэтому можно сделать, например, скругление и получить необычную форму блока:

```css
div {
  border-block: 20px solid white;
  border-radius: 40%;
}
```

<iframe title="Скругление рамок" src="../demos/border-rounding/" height="250"></iframe>

🎨 А если поэкспериментировать только со стилями `border-block`, то несложно изобразить фотоплёнку, флаг Австрии и ещё что в голову придёт:

```css
.film {
  background-color: #7b3f00;
  width: 300px;
  height: 200px;
  border-block: 30px dotted white;
}

.flag {
  background-color: white;
  width: 400px;
  height: 200px;
  border-block: 60px solid red;
}
```

<iframe title="Изображение фотоплёнки и флага с помощью рамок" src="../demos/border-film-and-flag/" height="250"></iframe>
