# TableOfContent_JS

# 🌐 Работа с DOM, BOM и событиями в JavaScript

## 📌 Что такое DOM?

---

<div align="center">
  <img src="https://hacks.mozilla.org/wp-content/uploads/2017/09/ezgif-2-2688553063.gif" width="800px" height="300px">
</div>

---

**DOM (Document Object Model)** — это программный интерфейс для HTML и XML-документов.  
Он представляет документ как дерево объектов, которое можно изменять с помощью JavaScript.

### 🖼 Структура DOM
Каждый узел документа — это:
- **Элемент** (например, `<div>`, `<p>`)
- **Атрибут** (например, `class`, `id`)
- **Текстовый узел** (содержимое тега)

Пример DOM-дерева:
```html
<html>
  <body>
    <h1>Заголовок</h1>
    <p>Параграф</p>
  </body>
</html>
```

# 📦 Что такое BOM?

---

<div align="center">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSUtJPejUWTnXddvZnk7g7b80ygLGWVHD9fXQ&s" width="800px" height="400px">
</div>

---

**BOM (Browser Object Model)** — это объектная модель браузера.
Она предоставляет доступ к функциям браузера, не связанным с содержимым страницы.

# 🔧 Основные объекты BOM:
* window — корневой объект (глобальный).
* navigator — информация о браузере (например, navigator.userAgent).
* screen — информация о экране (например, разрешение).
* location — URL-адрес страницы.
* history — история браузера (например, history.back()).

# 🔥 События в JavaScript
Событие — это сигнал о том, что что-то произошло.
Пример: клик мышью, нажатие клавиши, загрузка страницы.

# 🎯 Примеры событий:
* Мышь: click, dblclick, mouseover, mouseout
* Клавиатура: keydown, keypress, keyup
* Документ: DOMContentLoaded, scroll
* Форма: submit, focus, blur

# 📌 Как добавить обработчик событий?
### Через атрибут HTML
```html
<button onclick="alert('Клик!')">Нажми меня</button>
```
### Через свойство элемента
```js
const button = document.querySelector('button');
button.onclick = () => alert('Клик!');
```

### Через метод addEventListener
```js
const button = document.querySelector('button');
button.addEventListener('click', () => alert('Клик!'));
```

# 🛠 Методы DOM

---

<div align="center">
  <img src="https://miro.medium.com/v2/resize:fit:1400/1*lpyyiqvcKIlbTzq_gJPXCw.gif" width="800px" height="400px">
</div>

---


## 🔍 Поиск элементов
getElementById: Поиск по ID
```js
const element = document.getElementById('myId');
```
getElementsByClassName: Поиск по классу
```js
const elements = document.getElementsByClassName('myClass');
```
getElementsByTagName: Поиск по тегу
```js
const elements = document.getElementsByTagName('div');
```
querySelector: Первый элемент по CSS-селектору
```js
const element = document.querySelector('.myClass');
```
querySelectorAll: Все элементы по CSS-селектору
```js
const elements = document.querySelectorAll('.myClass');
```

# ✏️ Изменение содержимого
innerHTML: Изменяет HTML внутри элемента
```js
element.innerHTML = '<p>Новый текст</p>';
```
textContent: Изменяет только текст
```js
element.textContent = 'Новый текст';
```

# 🎨 Изменение стилей
style: Устанавливает CSS-стили элемента
```js
element.style.color = 'red';
element.style.fontSize = '20px';
```

# ✨ Работа с классами
classList.add: Добавляет класс
```js
element.classList.add('new-class');
```
classList.remove: Удаляет класс
```js
element.classList.remove('old-class');
```
classList.toggle: Переключает класс
```js
element.classList.toggle('active');
```
classList.contains: Проверяет наличие класса
```js
console.log(element.classList.contains('my-class'));
```

# 🧩 Полезные методы

---

<div align="center">
  <img src="https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fm2ja8tymo646or3emo07.gif" width="800px" height="400px">
</div>

---

## 📜 Создание элементов
document.createElement: Создает новый элемент
```js
const newElement = document.createElement('div');
newElement.textContent = 'Я новый!';
document.body.appendChild(newElement);
```

## 🧹 Удаление элементов
remove: Удаляет элемент
```js
element.remove();
```

## ⛓ Манипуляции с DOM-узлами
appendChild: Добавляет элемент в конец
```js
parent.appendChild(child);
```
insertBefore: Вставляет перед элементом
```js
parent.insertBefore(newElement, referenceElement);
```

# 🔮 Пример комбинирования:
```html
<div id="app">
  <button id="btn">Добавить элемент</button>
</div>
<script>
  const app = document.getElementById('app');
  const button = document.getElementById('btn');
  
  button.addEventListener('click', () => {
    const newDiv = document.createElement('div');
    newDiv.textContent = 'Я новый элемент!';
    newDiv.style.color = 'blue';
    app.appendChild(newDiv);
  });
</script>
```

---

<div align="center">
  <img src="https://a.d-cd.net/fGkj61MC91njUbKjZUahzEm1-IA-960.jpg" width="600px" height="300px">
</div>

---
