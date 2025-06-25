# Язык разметки текста HTML

# Что такое HTML?
HTML - HyperText Markup Language - язык гипертектовой разметки - является языком разметки электронных документов, указывающим программа просмотра HTML-страниц (браузерам) форму представления описанной в документе информации
## создание HTML документа
<br> 1. Создать текстовый документ с расширением .txt
<br> 2. Изменить расширение на .html
<br> 3. Открыть документ с помощью программы блокнот
<br> 4. С помощью языка HTML создать содержимое документа
## Структура HTML документа
<br> конструкции, заключенные в угловые скобки `<>`, называются тегом 
<br> парные теги: `<B> </B>` одинарные теги: `<p>`
<br> раздел HTML: определяет специфику документа и даёт браузеру информацию о том, что документ разработан с помощью этого языка
<br> раздел HEAD: предназначен для указания заголовков созданного документа
<br> раздел BODY: содержательная часть, которая выводится браузером на экран монитора пользователя
## расположение разделов HTML в документе 
```
<HTML>
  <HEAD>
    содержимое раздела
  </HEAD>
<BODY
  содержимое раздела
</BODY>
</HTML>
```
## Содержимое раздела HEAD
- TITLE `<TITLE> </TITLE>`: название документа
- LINK: связь между документами
- META: метаопределения
- STYLE: описывает стилевые шаблоны документа
- SCRIPT: содержит код исполняемых сценариев
## Метаопределение `<META>`
<br> Содержит параментры предназначенные для описания внутренних свойств для описания внутренних свойств HTML-файла
<br> Два типа данных `HTTP-EQUIV` и `NAME`
<br> Команда браузеру ровно через 10 секунд перенаправить посетителя по указанному адресу
```
<META HTTP-EQUIV = "refresh" content "10;
URL = http://www.site.ru>
```
<br> Задание набора ключевых слов
```
<META NAME = "keywords" CONTENT = "ключевое слово 1, ключевое слово 2">
```
<br> Описание документа, которое выводится рядом с ссылкой на найденный интернет-ресурс
```
<MENA NAME = "description" CONTENT = "описание документа">
```
## Раздел BODY
<br>Может содержать следующие группы параметров:
- Фон:
  - BGCOLOR – цвет фона
  - BACKGROUND – фоновый рисунок
- Границы документа:
  - TOPMARGIN, BOTTOMMARGIN, LEFTMARGIN, RIGHTMARGIN – отступы от краёв
- Текст:
  - TEXT – цвет основного текста
- Гиперссылки:
  - LINK – цвет непосещённых ссылок
  - VLINK – цвет посещённых ссылок
  - ALINK – цвет активных ссылок
<br> Пример:
```
<BODY BGCOLOR="green" TEXT="yellow" TOPMARGIN="15">
  Пример
</BODY>
```
## Установка цвета
<br> Цвета в HTML задаются с помощью модели RGB (Red, Green, Blue).
<br> Варианты указания белого цвета:
```
<BODY BGCOLOR="White">
<BODY BGCOLOR="#FFFFFF">
<BODY BGCOLOR="255,255,255">
```
## Форматирование текста
Теги логического форматирования:
- `<ACRONYM>` – для аббревиатур
- `<CITE>` – цитаты (курсив)
- `<DEL>` – удалённый текст (зачёркнутый)
- `<EM>` – интонационное выделение (курсив)
- `<H1>-<H6>` – заголовки разного уровня
- `<STRONG>` – важный текст (жирный)

<br> Теги физического форматирования:
- `<B>` – жирный текст
- `<I>` – курсив
- `<U>` – подчёркивание
- `<SUB>` – нижний индекс
- `<SUP>` – верхний индекс
- `<FONT>` – настройки шрифта (цвет, размер, название)
<br> Пример:
```
<FONT FACE="Tahoma, Arial" COLOR="red" SIZE="4">
  Текст с форматированием
</FONT>
```
## Структурное форматирование
- `<P>` – абзац (может включать выравнивание: ALIGN="left|center|right|justify")
- `<DIV>` – текстовый блок с переносом
- `<SPAN>` – текстовый блок без изменения структуры
- `<BR>` – перенос строки
- `<HR>` – горизонтальная линия (параметры: WIDTH, SIZE, COLOR, ALIGN)
<br> Пример горизонтальной линии:
```
<HR WIDTH="90%" SIZE="5" ALIGN="center" COLOR="#CC3399" NOSHADE>
```
## Гиперссылки
<br> Внешние ссылки:
```
<A HREF="http://www.tpu.ru">Томский политехнический университет</A>
```
<br> Ссылка на email:
```
<A HREF="mailto:mail@site.ru?Subject=Здравствуйте!">Отправить письмо</A>
```
<br> Внутренние ссылки:
```
<A HREF="#section">Перейти к разделу</A>
...
<A NAME="section"></A>
```
## Списки
<br> Нумерованные списки `(<OL>)`:
  - TYPE="1|A|a|I|i" – стиль нумерации
  - START="n" – начать с номера n

<br> Маркированные списки `(<UL>)`:
  - TYPE="disc|circle|square" – стиль маркера
<br> Вложенные списки: комбинация `<UL>` и `<OL>`
<br> Пример нумерованного списка:
```
<OL TYPE="A">
  <LI>Пункт 1</LI>
  <LI>Пункт 2</LI>
</OL>
```
## Таблицы
- `<TABLE>` – контейнер для таблицы
- `<TR>` – строка таблицы
- `<TD>` – ячейка таблицы
- `<TH>` – заголовок ячейки (жирный)
- `<CAPTION>` – заголовок таблицы

<br> Параметры таблицы:
1. BORDER – рамка
2. CELLSPACING – расстояние между ячейками
3. CELLPADDING – отступ внутри ячеек
4. COLSPAN и ROWSPAN – объединение ячеек
<br> Пример:
```
<TABLE BORDER="1" ALIGN="center">
  <TR>
    <TH>Заголовок</TH>
    <TD>Ячейка</TD>
  </TR>
</TABLE>
```
## Графика
- `<IMG>` – вставка изображения
- `SRC` – путь к изображению
- `WIDTH` и `HEIGHT` – размеры
- `ALIGN` – выравнивание (например, left, right)
<br> Пример:
```
<IMG SRC="logo.jpg" ALIGN="left" WIDTH="100">
```
## Комментарии
Комментарии не отображаются на странице, но помогают в разработке:
```
<!-- Это комментарий -->
```


# Лекция 1: Введение в Web
# Основы Web
Базовый сценарий работы web-приложения
1. Пользователь вводит URL
2. Браузер загружает HTML-документ
3. Браузер анализирует (парсит) HTML и загружает дополнительные ресурсы
4. Браузер отображает (рендерит) страницу

## Структура URL
Пример: `http://mi-ami.ru:8080/profile/account.html?gender=male&age=13#comments`
- `http` - протокол
- `mi-ami.ru` - доменное имя
- `8080` - TCP порт
- `/profile/account.html` - путь к документу
- `?gender=male&age=13` - параметры запроса
- `#comments` - якорь
## Документы и ресурсы
Типы документов (MIME-типы):
`text/html`
`text/css`
`text/javascript`
`image/png`
`video/mp4`
<br> Виды документов:
- Статические - файлы на сервере с постоянным адресом
- Динамические - создаются при каждом запросе, зависят от внешних факторов
<br> Примеры подключения ресурсов:
```
<link rel="stylesheet" href="/css/index.css">
<script src="http://code.jquery.com/jquery-2.1.4.js"></script>
<img src="pictures/network.png" width="200">
```
## HTTP протокол
Основные сетевые протоколы:
- `TCP`
- `UDP`
- `HTTP (работает поверх TCP)`
- `FTP`
- `SSH`
<br> Структура HTTP:
1. Клиент отправляет запрос
2. Сервер обрабатывает запрос и возвращает ответ
<br> Структура HTTP-запроса:
- Метод (GET, POST, PUT, DELETE)
- URL
- Заголовки
- Тело (может отсутствовать)
<br> Структура HTTP-ответа:
- Статус ответа (1xx-5xx)
- Заголовки
- Тело
<br> Пример HTTP-запроса:
```
GET http://www.ru/robots.txt HTTP/1.0
Accept: text/html, text/plain
User-Agent: curl/7.64.1
If-Modified-Since: Fri, 24 Jul 2015 22:53:05 GMT
```
<br> Пример HTTP-ответа:
```
HTTP/1.1 404 Not Found
Server: nginx/1.5.7
Date: Sat, 25 Jul 2015 09:58:17 GMT
Content-Type: text/html; charset=iso-8859-1
Connection: close

<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<HTML><HEAD>...
```
# HTML
Базовая структура HTML-документа:
```
<!DOCTYPE html>
<html>
  <head>
    <title>Страница</title>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
    <meta name="description" content="Сайт">
    <link rel="stylesheet" href="./style.css">
  </head>
  <body id="the_body">
    <p class="article">...</p>
    <script src="./script.js"></script>
  </body>
</html>
```
<br> Основные теги:
- `html` - корневой элемент
- `head` - метаинформация
- `body` - содержимое страницы
- `title` - заголовок страницы
- `meta` - метаданные
- `link` - подключение ресурсов
- `script` - JavaScript
<br>Теги внутри body:
- `h1-h6` - заголовки
- `p` - параграфы
- `div` - блочный контейнер
- `span` - строчный контейнер
- `a` - гиперссылки
- `img` - изображения
- `ul/ol/li` - списки
## Гиперссылки:
```
<a href="http://iu5.bmstu.ru" target="_blank">Ссылка</a>
```
## Формы:
```
<form method="POST">
  <input name="image" type="file">
  <input name="id" type="hidden" value="3">
  <input name="nick" type="text">
  <input type="submit" value="Отправить">
</form>
```
# CSS
Способы подключения CSS:
1. Внешний файл:
```
<link rel="stylesheet" href="style.css">
```
2. В HTML коде:
```
<style>...</style>
```
3. В атрибуте style:
```
<img style="margin: 3px" src="...">
```
## Основные CSS свойства:
- `width, height` - размеры
- `margin, padding` - отступы
- `display` - тип отображения
- `color` - цвет текста
- `background` - фон
- `font` - шрифт
- `text-align` - выравнивание текста

## Селекторы:
Универсальный: `*`
По тегу: `p`
По классу: `.btn`
По id: `#userpic`
Контекстные: `div.article a`
Дочерние: `a > img`
Соседние: `h2.sic + p`
Группировка: `h1, h2`

## Наследование и приоритеты:
<br> Стили наследуются от родительских элементов. В случае конфликта:
1.Применяется более специфичный селектор
2. Если специфичность равна - применяется последний объявленный стиль
3. `!important` переопределяет все правила

# JavaScript
## Способы подключения JavaScript:
1. Внешний файл:
```
<script src="./jquery.js"></script>
```
2. В HTML коде:
```
<script>...</script>
```
<br> Пример JavaScript кода:
```
<!DOCTYPE HTML>
<html>
<body>
  <p>Перед скриптом...</p>
  <script>
    alert('Привет, мир!');
  </script>
  <p>...После скрипта.</p>
</body>
</html>
```

# Лекция 2: JavaScript
# Основы JavaScript
## Переменные
<br> Объявление переменных:
- `let` - современный способ (блочная область видимости)
- `var` - устаревший способ (функциональная область видимости)
- `const` - константа (нельзя переопределять)
```
let message = "hello";
message = 123456; // нет ошибки
```
## Типизация
<br> JavaScript - слабо типизированный язык. Автоматическое преобразование типов:
```
"" == 0 // true
"0" == 0 // true
"" == "0" // false
"0" == false // true
```
## Математические операции
```
const a = 3 + 2; // 5
const b = a - 5; // 0
const c = -b; // -0
const d = 10 % 2; // 0
const e = d * 2; // 0
const f = d / 2; // 0
let a = 0;
a += 2; // 2
a++; // 3
```
## Операторы сравнения
```
3 > 2 // true
4 >= 1 // true
1 < 3 // true
2 <= 2 // true
false == "" // true
0 == 0 // true
false != 1 // true
false !== true // true
```
## Условные операторы
```
if (year == 2007) {
  alert('Верните меня туда');
} else {
  alert('Эх...');
}

// Тернарный оператор
const year = (условие) ? 2007 : 2023;
```
## Циклы
```
while (condition) {
  // тело цикла
}

do {
  // тело цикла
} while (condition);

for (let i = 0; i < 10; i++) {
  // тело цикла
}
```
## Функции
Function Declaration vs Function Expression
```
// Function Declaration
function sum(a, b) {
  return a + b;
}

// Function Expression
let sum = function(a, b) {
  return a + b;
};
```
<br> Function Expression создается, когда выполнение доходит до него, и затем уже может использоваться
<br> Function Declaration может быть вызваа раньше, чем она объявлена
## Стрелочные функции
```
const sum1 = (a, b) => a + b;

const sum2 = (a, b) => {
  let result = a + b;
  return result;
};
```
# Объекты
## Создание объектов
```
let user = new Object(); // конструктор
let user = {}; // литерал
```
## Работа с объектами
```
const user = {
  name: "John",
  age: 30
};

console.log(user.name); // "John"
console.log(user["age"]); // 30

user.isAdmin = true;
const key = 'age';
user[key] = 18;
```
## Контекст this
```
let user = { name: "John" };
let admin = { name: "Admin" };

function sayHi() {
  alert(this.name);
}

user.f = sayHi;
admin.f = sayHi;

user.f(); // John
admin.f(); // Admin
``` 
## Псевдо-ООП
```
function User(name) {
  this.name = name;
  this.sayHi = function() {
    alert("Меня зовут: " + this.name);
  };
}

let john = new User("John");
john.sayHi(); // Меня зовут: John
```
# Типы данных
## Примитивы
- string
- number
- boolean
- symbol
- null
- undefined
- bigint
## Числа
```
// Запись чисел
1000000000
1_000_000_000
1e9
1e-9
0b11111111 // 255 (binary)
0o377 // 255 (octal)
0xFF // 255 (hex)

// Методы
let num = 255;
num.toString(16); // "ff"
num.toString(2); // "11111111"

// Округление
Math.floor(3.1) // 3
Math.ceil(3.1) // 4
Math.round(3.6) // 4
Math.trunc(3.1) // 3

// Проверки
isNaN(NaN) // true
isFinite("15") // true
Number.isNaN("str") // false
```
## Строки
```
let str = "Hello";
str[0]; // "H"
str.at(0); // "H"
str.length; // 5

// Методы
str.toUpperCase(); // "HELLO"
str.toLowerCase(); // "hello"
str.indexOf("el"); // 1
str.includes("el"); // true

// Подстроки
str.slice(0, 2); // "He"
str.substring(2, 4); // "ll"
str.substr(2, 2); // "ll"
```
## Массивы
Создание и доступ
```
let fruits = ["Яблоко", "Апельсин", "Слива"];
fruits[0]; // "Яблоко"
fruits.at(-1); // "Слива"
```
## Методы массивов
```
// Добавление/удаление
fruits.pop(); // удаляет последний
fruits.push("Груша"); // добавляет в конец
fruits.shift(); // удаляет первый
fruits.unshift("Яблоко"); // добавляет в начало

// Поиск
fruits.indexOf("Апельсин"); // 1
fruits.includes("Апельсин"); // true

// Преобразование
fruits.slice(1, 3); // ["Апельсин", "Слива"]
fruits.concat(["Банан"]); // ["Яблоко", "Апельсин", "Слива", "Банан"]
fruits.join(", "); // "Яблоко, Апельсин, Слива"

// Перебор
for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}

fruits.forEach(fruit => console.log(fruit));

// Функциональные методы
fruits.filter(fruit => fruit.length > 5);
fruits.map(fruit => fruit.toUpperCase());
fruits.reduce((sum, fruit) => sum + fruit.length, 0);
```
## Современные возможности
Деструктуризация
```
// Массив
let [firstName, surname] = ["Ilya", "Kantor"];

// Объект
let {title, width, height} = {title: "Menu", width: 100, height: 200};

// Вложенная
let options = {
  size: { width: 100, height: 200 },
  items: ["Cake", "Donut"]
};
let { size: { width }, items: [item1] } = options;
```
## Map и Set
```
// Map
let map = new Map();
map.set("1", "str1");
map.get("1"); // "str1"

// Set
let set = new Set();
set.add("John");
set.add("John"); // не добавится повторно
```
## JSON
```
let student = {
  name: 'John',
  age: 30
};

let json = JSON.stringify(student);
let parsed = JSON.parse(json);
```
# Классы
## Базовый синтаксис
```
class User {
  constructor(name) {
    this.name = name;
  }

  sayHi() {
    alert(this.name);
  }
}

let user = new User("Иван");
user.sayHi();
```
## Наследование
```
class Animal {
  constructor(name) {
    this.speed = 0;
    this.name = name;
  }
  
  run(speed) {
    this.speed = speed;
  }
}

class Rabbit extends Animal {
  hide() {
    alert(`${this.name} прячется!`);
  }
}
```
## Статические методы и свойства
```
class Article {
  static publisher = "Илья Кантор";
  
  static compare(a, b) {
    return a.date - b.date;
  }
}
```
## Приватные свойства
```
class CoffeeMachine {
  #waterLimit = 200;
  
  #checkWater(value) {
    if (value < 0) throw new Error("Отрицательный уровень воды");
  }
}
```

# Лекция 3: Углубленный JavaScript
# Продвинутая работа с функциями
## Rest-оператор
<br> Собирает все аргументы функции в массив:
```
function sumAll(...args) {
  let sum = 0;
  for (let arg of args) sum += arg;
  return sum;
}
```
## Spread-оператор
<br> Разворачивает массив в список аргументов:
```
const arr1 = [0, -2, 1, 5];
const arr2 = [100, 200, 300, -322];
console.log(Math.max(...arr1, ...arr2));
```
## Замыкания
<br> Замыкание - это функция, которая запоминает свои внешние переменные и может получить к ним доступ. В JavaScript все функции являются замыканиями (кроме новых Function).
<br> Как это работает:
1. При создании функции она запоминает текущее лексическое окружение в `[[Environment]]`
2. При вызове функции создается новое лексическое окружение с внешней ссылкой на сохраненное `[[Environment]]`
3. Если функция обращается к переменной, поиск идет по цепочке лексических окружений
```
function makeCounter() {
  let count = 0;
  return function() {
    return count++;
  };
}
let counter = makeCounter();
alert(counter()); // 0
alert(counter()); // 1
```
## Лексическое окружение
<br> В JavaScript у каждой выполняемой функции, блока кода и скрипта есть связанный с ними внутренний (скрытый) объект, называемый лексическим окружением (LexicalEnvironment). Этот объект состоит из двух частей:
1. Environment Record - объект, хранящий все локальные переменные (а также значение `this` и другую информацию)
2. Ссылка на внешнее лексическое окружение - соответствует коду снаружи текущих фигурных скобок
<br> Ключевые особенности:
- Переменная - это свойство специального внутреннего объекта Environment Record
- Работа с переменными = работа со свойствами этого объекта
- Function Declaration инициализируются сразу при создании лексического окружения
- Все функции при создании получают скрытое свойство `[[Environment]]`, ссылающееся на лексическое окружение их создания
## Контекст выполнения и this
<br> Привязка контекста
<br> Методы для работы с контекстом:
```
// call - вызывает функцию с указанным контекстом
func.call(context, arg1, arg2);

// apply - аналогично call, но аргументы передаются массивом
func.apply(context, [arg1, arg2]);

// bind - создает новую функцию с привязанным контекстом
let boundFunc = func.bind(context);
```
## Декораторы
<br> Функция-обертка для кеширования результатов:
```
function cachingDecorator(func) {
  let cache = new Map();
  return function(x) {
    if (cache.has(x)) return cache.get(x);
    let result = func.call(this, x);
    cache.set(x, result);
    return result;
  };
}
```
## Прототипы и наследование
<br> В JavaScript объекты имеют специальное скрытое свойство `[[Prototype]]`, которое либо равно `null`, либо ссылается на другой объект (прототип). Когда мы хотим прочитать свойство из объекта, а оно отсутствует, JavaScript автоматически берет его из прототипа.
<br> Основные концепции:
- Прототип используется только для чтения свойств
- Операции записи/удаления работают непосредственно с объектом
- Цикл `for..in` перебирает как собственные, так и унаследованные свойства
- Метод `Object.create(proto)` создает пустой объект с заданным `[[Prototype]]`
<br> Прототипное наследование
```
let animal = { eats: true };
let rabbit = { jumps: true };
rabbit.__proto__ = animal; // rabbit наследует от animal
alert(rabbit.eats); // true
```
## Классы и наследование
<br> Классы в JavaScript - это "синтаксический сахар" над существующим прототипным наследованием.
<br> Основные концепции:
- Конструктор класса вызывается при создании объекта через `new`
- Методы класса хранятся в `ClassName.prototype`
- Классы могут наследовать друг от друга через `extends`
- `super` используется для вызова родительского конструктора/методов
- Статические методы принадлежат самому классу, а не его экземплярам
```
class Animal {
  constructor(name) {
    this.speed = 0;
    this.name = name;
  }
  run(speed) {
    this.speed = speed;
  }
}

class Rabbit extends Animal {
  hide() {
    alert(`${this.name} прячется!`);
  }
}
```
## Модули в JavaScript
<br> Модули позволяют разбивать код на отдельные файлы с четко определенными интерфейсами.
<br> Основные концепции:
- Каждый модуль имеет свою область видимости
- Для экспорта используются директивы `export`
- Для импорта - `import`
- Модуль выполняется только один раз при первом импорте
- Поддерживаются как именованные, так и экспорт по умолчанию
<br> Типы модульных систем:
- ESM (ECMAScript Modules) - современный стандарт
- CommonJS - используется в Node.js
- AMD - асинхронные модули для браузеров
- UMD - универсальные модули
<br> Импорт/экспорт
```
// say.js
export function sayHi(user) {
  alert(`Hello, ${user}!`);
}

// main.js
import { sayHi } from './say.js';
sayHi('John');
```
<br> Динамический импорт
```
let { hi, bye } = await import('./say.js');
hi();
```
## Обработка ошибок
<br> JavaScript использует механизм `try...catch` для обработки исключений.
<br> Основные концепции:
- Ошибки можно генерировать через `throw`
- Можно создавать собственные классы ошибок, наследуясь от `Error`
- Блок `finally` выполняется в любом случае
- Объект ошибки содержит:
  - `name` - тип ошибки
  - `message` - текстовое сообщение
  - `stack` - стек вызовов
<br>Иерархия встроенных ошибок:
- `Error` - базовая ошибка
- `SyntaxError` - синтаксическая ошибка
- `ReferenceError` - ссылка на несуществующую переменную
- `TypeError` - операция над значением неверного типа
<br> Try...catch
```
try {
  // код, который может вызвать ошибку
} catch (err) {
  // обработка ошибки
  alert(err.name); // имя ошибки
  alert(err.message); // сообщение об ошибке
} finally {
  // выполнится в любом случае
}
```
<br> Пользовательские ошибки
```
class ValidationError extends Error {
  constructor(message) {
    super(message);
    this.name = "ValidationError";
  }
}

throw new ValidationError("Ошибка валидации");
```
## Регулярные выражения
<br> Создание и использование
```
let regexp = /шаблон/флаги;
regexp = new RegExp("шаблон", "флаги");

// Методы работы:
str.match(regexp); // поиск совпадений
str.replace(regexp, replacement); // замена
regexp.test(str); // проверка на совпадение
```
## Работа с событиями
<br> Браузерные события обрабатываются через систему погружения (capture) и всплытия (bubble).
<br> Основные концепции:
- События сначала идут вниз (погружение), затем вверх (всплытие)
- Обработчики можно назначать на любой фазе
- `event.stopPropagation()` останавливает всплытие
- `event.preventDefault()` отменяет действие по умолчанию
- Делегирование событий - назначение обработчика родителю
<br> Типы событий:
- События мыши (`click`, `mouseover` и др.)
- События клавиатуры (`keydown`, `keyup`)
- События форм (`submit`, `focus`)
- События документа/DOM (`DOMContentLoaded`)
<br> Обработчики событий
```
element.onclick = function(event) {
  alert(`Клик по ${event.target.tagName}`);
};

// Или с addEventListener:
element.addEventListener("click", handler);
element.removeEventListener("click", handler);
```
<br> Всплытие и погружение
```
// Погружение (capturing phase)
elem.addEventListener(..., {capture: true});

// Всплытие (bubbling phase) - по умолчанию
elem.addEventListener(..., false);

// Остановка всплытия:
event.stopPropagation();
```
<br> Пользовательские события
```
let event = new Event("click");
element.dispatchEvent(event);
```

# Лекция 4: Архитектура Web
# Внутреннее устройство браузера
<br> Процессы браузера:
- Network Process - обработка сетевых запросов
- Storage Process - управление хранилищами (cookie, cache)
- Device Process - взаимодействие с устройствами
- Renderer Process - рендеринг страниц (по одному на вкладку)
- GPU Process - обработка графики
- Plugin Process - работа с плагинами
<br> Критические этапы рендеринга:
1. Загрузка HTML - получение и парсинг HTML
2. Построение DOM - создание дерева документа
3. Построение CSSOM - анализ стилей
4. Формирование Render Tree - объединение DOM и CSSOM
5. Layout (компоновка) - расчет позиций и размеров
6. Paint (отрисовка) - отрисовка пикселей на экране
```
// Пример: отслеживание времени загрузки
window.addEventListener('load', () => {
  console.log('Страница полностью загружена');
});
```
## DOM, CSSOM и Render Tree
<br>Document Object Model (DOM)
```
<!-- Исходный HTML -->
<div class="header">
  <h1>Заголовок</h1>
  <p>Текст</p>
</div>
```
```
// Соответствующее DOM-дерево:
// - div.header
//   - h1
//     - "Заголовок"
//   - p
//     - "Текст"
```
## CSS Object Model (CSSOM)
```
.header { font-size: 16px; }
h1 { color: red; }
p { margin: 10px; }
```
## Render Tree
<br> Объединяет только видимые элементы с их стилями:
- Элементы с `display: none` не включаются
- `head`, `meta` и другие невидимые элементы исключаются

## Ограничения JavaScript в браузере
1. Нет доступа к файловой системе (кроме загрузки файлов через <input type="file">)
2. Ограниченный сетевой доступ (только через XMLHttpRequest, Fetch API)
3. Однопоточность (Web Workers имеют ограничения)
4. Нельзя запускать процессы (ограниченное взаимодействие с ОС)

## Работа с npm и модулями
Инициализация проекта:
```
npm init -y
```
<br> package.json:
```
{
  "name": "my-app",
  "version": "1.0.0",
  "scripts": {
    "start": "node index.js",
    "test": "jest"
  },
  "dependencies": {
    "lodash": "^4.17.21"
  },
  "devDependencies": {
    "webpack": "^5.75.0"
  }
}
```
<br> Подключение библиотек:
```
<!-- CDN -->
<script src="https://cdn.jsdelivr.net/npm/lodash@4.17.21/lodash.min.js"></script>

<!-- Локально через npm -->
import _ from 'lodash';
```
## Архитектурные принципы
<br> Основные методологии:
- DRY (Don't Repeat Yourself) - избегание дублирования кода
- KISS (Keep It Simple Stupid) - простота реализации
- SOLID - 5 принципов ООП:
  1. Single Responsibility
  2. Open-Closed
  3. Liskov Substitution
  4. Interface Segregation
  5. Dependency Inversion
<br> Декомпозиция приложения:
```
// Функциональная декомпозиция
// userModule.js
let user = null;

export function setUser(newUser) {
  user = newUser;
}

export function getUser() {
  return user;
}

// app.js
import { getUser } from './userModule.js';
console.log(getUser());
```
## Компонентный подход
<br> Пример компонента:
```
class ProductCard {
  constructor(parent, data) {
    this.parent = parent;
    this.data = data;
  }

  render() {
    this.parent.innerHTML = `
      <div class="product-card">
        <h3>${this.data.title}</h3>
        <img src="${this.data.image}" alt="${this.data.title}">
        <p>${this.data.price}</p>
      </div>
    `;
  }
}

// Использование
const card = new ProductCard(document.getElementById('container'), {
  title: "Телефон",
  image: "phone.jpg",
  price: "999$"
});
card.render();
```
## Паттерн MVC (Model-View-Controller)
<br> Модель (Model):
```
class ProductModel {
  constructor() {
    this.products = [];
  }

  async fetchProducts() {
    const response = await fetch('/api/products');
    this.products = await response.json();
    return this.products;
  }

  getProductById(id) {
    return this.products.find(p => p.id === id);
  }
}
```
<br> Представление (View):
```
class ProductView {
  constructor(controller) {
    this.controller = controller;
    this.element = document.getElementById('products');
  }

  render(products) {
    this.element.innerHTML = products.map(p => `
      <div class="product" data-id="${p.id}">
        <h2>${p.name}</h2>
        <p>${p.price}</p>
      </div>
    `).join('');

    this.element.addEventListener('click', (e) => {
      const productElement = e.target.closest('.product');
      if (productElement) {
        const id = productElement.dataset.id;
        this.controller.handleProductClick(id);
      }
    });
  }
}
```
<br> Контроллер (Controller):
```
class ProductController {
  constructor() {
    this.model = new ProductModel();
    this.view = new ProductView(this);
  }

  async init() {
    const products = await this.model.fetchProducts();
    this.view.render(products);
  }

  handleProductClick(id) {
    const product = this.model.getProductById(id);
    console.log('Product selected:', product);
    // Можно открыть детальную страницу и т.д.
  }
}

// Инициализация
const controller = new ProductController();
controller.init();
```
## Роутинг и History API
<br> Реализация простого роутера:
```
class Router {
  constructor() {
    this.routes = {};
    this.currentRoute = '';
    window.addEventListener('popstate', () => this.handleRouting());
  }

  register(path, view) {
    this.routes[path] = view;
  }

  navigate(path) {
    history.pushState({}, '', path);
    this.handleRouting();
  }

  handleRouting() {
    const path = window.location.pathname;
    const view = this.routes[path] || this.routes['/404'];
    if (view) {
      view.render();
    }
  }
}

// Использование
const router = new Router();
router.register('/', homeView);
router.register('/products', productsView);
router.navigate('/products');
```
<br> History API методы:
```
history.pushState(state, title, url); // Добавляет запись в историю
history.replaceState(state, title, url); // Заменяет текущую запись
window.onpopstate = (event) => { /* Обработка навигации */ };
```
## Архитектура CSS
<br> Проблемы плохой архитектуры:
1.Глубокая вложенность:
```
#main-nav ul li ul li ol span div { ... }
```
2. Зависимость от контекста:
```
.header .button { ... }
.footer .button { ... }
```
3. Конфликты имен:
```
/* В разных файлах */
.title { ... }
.title { ... }
```
<br> Решения:
1. CSS Modules:
```
// styles.module.css
.button { color: red; }

// component.js
import styles from './styles.module.css';
element.innerHTML = `<button class="${styles.button}">Click</button>`;
```
2. CSS-in-JS (JSS):
```
const styles = {
  button: {
    color: 'red',
    '&:hover': {
      color: 'darkred'
    }
  }
};

const { classes } = jss.createStyleSheet(styles).attach();
element.innerHTML = `<button class="${classes.button}">Click</button>`;
```
3. Методология БЭМ:
```
/* Блок */
.menu { ... }

/* Элемент */
.menu__item { ... }

/* Модификатор */
.menu__item--active { ... }
```
## Лучшие практики архитектуры CSS
1. Разделение структуры и оформления:
```
/* Плохо */
.article .header { color: blue; }

/* Хорошо */
.article-header { color: blue; }
```
2. Использование CSS-переменных:
```
:root {
  --primary-color: #4285f4;
  --secondary-color: #34a853;
}

.button {
  background-color: var(--primary-color);
}
```
3. Компонентный подход:
```
components/
  button/
    button.css
    button.js
    button.test.js
  header/
    header.css
    header.js
```
# Лекция 5: Node.js
# Поиск сервера
- Браузер использует DNS для получения IP-адреса сервера.
- DNS работает как распределённая "контактная книга" интернета.
## TCP-соединение
- Устанавливается через тройное рукопожатие:
  - SYN → SYN/ACK → ACK.
- Уровни сетевой модели OSI:
  - Приложение (HTTP, DNS), Транспорт (TCP, UDP), Сетевой (IP), Канальный (Ethernet), Физический.
## Клиент-серверная модель
- Клиенты (браузеры, приложения) отправляют запросы, серверы обрабатывают и возвращают ответы.
- Примеры: статические страницы, SSR (рендеринг на сервере), веб-приложения с API.
## Node.js
- Среда выполнения JavaScript на движке V8.
- Используется для:
  - Бэкенда (веб-серверы, BFF, микросервисы).
  - Десктопных приложений (Electron.js).
  - Консольных утилит.
- Преимущества:
  - Высокая производительность (асинхронность, Event Loop).
  - Простота создания сервера (15 строк кода).
- Недостатки:
  - Отсутствие строгой типизации (риск ошибок).
  - Нет многопоточности.
  - Медленные вычисления.
## TypeScript
<br> Надмножество JavaScript с статической типизацией.
- Преимущества:
  - Проверка типов на этапе компиляции.
  - Поддержка интерфейсов, кортежей, ООП.
  - Совместимость с JS.
<br> Пример:
```
interface Person { name: string; age: number; }
function greet(person: Person) { return `Hello, ${person.name}!`; }
```
## Nest.js
<br> Фреймворк для серверных приложений на TypeScript.
<br> Особенности:
- Готовая архитектура (MVC, DI).
- Поддержка gRPC, валидации.
<br> Пример контроллера:
```
@Controller('stocks')
export class StocksController {
  @Get() findAll() { return this.stocksService.findAll(); }
}
```
<br> Пример кода для простого сервера на Node.js:
```
const http = require('http');
const HOST = 'localhost';
const PORT = 8000;

const handler = (req, res) => {
  res.writeHead(200);
  res.end('Hello, Node.js!');
};

const server = http.createServer(handler);
server.listen(PORT, HOST, () => {
  console.log(`Server running at http://${HOST}:${PORT}`);
});
```
<br> `SSR`: Рендеринг страниц на сервере.
<br> `BFF`: Backend For Frontend (прокси для агрегации данных).
<br> `REST`: Передача состояния клиента в каждом запросе.
<br> `Event Loop`: Механизм асинхронности в Node.js.

# Лекция 6: AJAX
# Основы AJAX
<br> AJAX (Asynchronous JavaScript and XML) — технология, позволяющая отправлять и получать данные с сервера без перезагрузки страницы.
<br> AJAX — асинхронные HTTP-запросы.
<br> Принцип работы:
- Использует объект `XMLHttpRequest` (XHR).
- Поддерживает асинхронные и синхронные запросы.
- Форматы данных: JSON, XML, HTML, текстовые файлы.
<br> Пример асинхронного запроса:
```
let xhr = new XMLHttpRequest();
xhr.open('GET', '/api/data');
xhr.send();

xhr.onload = function() {
  if (xhr.status === 200) {
    console.log('Данные:', xhr.response);
  } else {
    console.error('Ошибка:', xhr.status);
  }
};
```
## Форматы данных
- JSON: Универсальный формат для передачи объектов.
```
{
  "name": "John",
  "age": 30,
  "courses": ["html", "css", "js"]
}
```
- Blob: Для работы с бинарными данными (например, файлами).
```
const blob = new Blob([binaryData], { type: 'application/octet-stream' });
```
- FormData: Для отправки данных форм.
```
const formData = new FormData();
formData.append('file', fileInput.files[0]);
```
## CORS (Cross-Origin Resource Sharing)
CORS — механизм кросс-доменных запросов.
<br> Проблема: Браузер блокирует запросы к другому домену (Same Origin Policy).
<br> Решение:
<br> CORS-заголовки на сервере:
```
Access-Control-Allow-Origin: https://yourdomain.com
Access-Control-Allow-Methods: GET, POST
```
<br> Проксирование: Запросы отправляются через сервер фронтенда.
<br> Типы запросов:
1. Простые: `GET/POST` с ограниченными заголовками.
2. Непростые: Требуют предзапроса `OPTIONS`.
<br> Пример предзапроса:
```
OPTIONS /api/data
Access-Control-Request-Method: PATCH
Access-Control-Request-Headers: Content-Type, API-Key
```
## Хранение данных на клиенте
<br> Cookies:
- Маленький размер (~4 КБ).
- Используются для аутентификации и сессий.
- Параметры: `Expires`, `Secure`, `SameSite`.
```
document.cookie = "session_id=123; Secure; SameSite=Lax";
```
<br> LocalStorage:
- Хранение ключ-значение (до 5 МБ).
```
localStorage.setItem('theme', 'dark');
```
<br> IndexedDB:
- Клиентская база данных для сложных структур.

## Инструменты
<br> Postman: Для тестирования API.
<br> Вкладка Network в DevTools: Анализ запросов.
<br> Пример POST-запроса в Postman:
```
{
  "title": "Новая акция",
  "text": "Скидка 20%!"
}
```
## Безопасность
<br> SameSite Cookie:
- `Strict`: Куки только с того же сайта.
- `Lax`: Куки при переходе по ссылке.
- `None`: Разрешает кросс-доменные куки (требует `Secure`).
<br> Пример заголовка:
```
Set-Cookie: session=abc123; SameSite=Lax; Secure
```

# Лекция 7: Асинхронный JavaScript
# Введение в асинхронность
<br> Проблема синхронного выполнения кода
<br> JavaScript является однопоточным языком, что означает выполнение кода последовательно, строка за строкой. Однако при работе с внешними ресурсами (загрузка скриптов, запросы к серверу) это становится проблемой.
<br> Пример проблемы:
```
function loadScript(src) {
  let script = document.createElement('script');
  script.src = src;
  document.head.append(script);
}

loadScript('https://cdnjs.cloudflare.com/ajax/libs/lodash.js/3.2.0/lodash.js');
alert('Ура, скрипт загрузился!'); // Сработает ДО фактической загрузки скрипта
```
<br> Решение через колбэки
<br> Для решения проблемы используются функции обратного вызова (callback):
```
function loadScript(src, callback) {
  let script = document.createElement('script');
  script.src = src;
  
  script.onload = () => callback(script);
  script.onerror = () => callback(null);
  
  document.head.append(script);
}

loadScript('https://cdnjs.cloudflare.com/...', (script) => {
  if (!script) {
    alert('Ошибка загрузки скрипта!');
    return;
  }
  
  alert(`Скрипт ${script.src} загружен`);
  alert(_.VERSION); // Используем функции из загруженного скрипта
});
```
## Event Loop и очередь задач
<br> Основные понятия асинхронного выполнения
<br> JavaScript использует механизм Event Loop для обработки асинхронных операций. Вот как это работает:
1. `Call Stack` - стек вызовов, где выполняются синхронные операции
2. `Microtask Queue` - очередь для микротасков (промисы, `MutationObserver`)
3. `Macrotask Queue` - очередь для макротасков (`setTimeout`, `setInterval`, `UI rendering`)
4. `Event Loop` - механизм, который определяет порядок выполнения задач
```
Схема выполнения:
Call Stack → Microtasks → Macrotasks → Render
```
<br> Пример работы `Event Loop`
```
console.log('Start');

setTimeout(() => console.log('Timeout'), 0);

Promise.resolve()
  .then(() => console.log('Promise 1'))
  .then(() => console.log('Promise 2'));

console.log('End');

// Вывод:
// Start
// End
// Promise 1
// Promise 2
// Timeout
```
## Проблемы колбэков и их решение
<br> Callback Hell (Ад колбэков)
<br> При вложенных асинхронных операциях код становится сложным для чтения и поддержки:
```
loadScript('script1.js', () => {
  loadScript('script2.js', () => {
    loadScript('script3.js', () => {
      loadScript('script4.js', () => {
        // И так далее...
      });
    });
  });
});
```
## Проблемы с обработкой ошибок
<br> Ошибки в асинхронных колбэках сложно обрабатывать:
```
try {
  loadScript('script.js', () => {
    throw new Error('Ошибка в колбэке!');
  });
} catch (e) {
  // Этот блок НЕ перехватит ошибку из колбэка
  console.error(e);
}
```
## Промисы (Promises)
<br> Основы промисов
<br> Промис - это объект, представляющий результат асинхронной операции. Он может находиться в одном из трех состояний:
1. `pending` - ожидание
2. `fulfilled` - успешно выполнено
3. `rejected` - выполнено с ошибкой
<br> Пример создания промиса:
```
const promise = new Promise((resolve, reject) => {
  // Асинхронная операция
  setTimeout(() => {
    const success = Math.random() > 0.5;
    if (success) {
      resolve('Успех!');
    } else {
      reject(new Error('Ошибка!'));
    }
  }, 1000);
});

promise
  .then(result => console.log(result))
  .catch(error => console.error(error));
```
## Цепочки промисов
<br> Промисы можно объединять в цепочки:
```
loadScript('script1.js')
  .then(() => loadScript('script2.js'))
  .then(() => loadScript('script3.js'))
  .then(() => console.log('Все скрипты загружены'))
  .catch(error => console.error('Ошибка загрузки:', error));
```
## Комбинации промисов
1. `Promise.all` - ожидает выполнение всех промисов
2. `Promise.race` - возвращает результат первого выполнившегося промиса
3. `Promise.any` - возвращает первый успешно выполнившийся промис
4. `Promise.allSettled` - ждет завершения всех промисов (успешных и с ошибкой)
<br> Пример `Promise.all`:
```
Promise.all([
  fetch('/user/1'),
  fetch('/user/2'),
  fetch('/user/3')
])
.then(users => {
  console.log('Все пользователи:', users);
})
.catch(error => {
  console.error('Ошибка загрузки:', error);
});
```
## Async/Await
<br> Основы async/await
<br> Async/await - это синтаксический сахар над промисами, делающий асинхронный код более читаемым.
```
async function loadUserData() {
  try {
    const user = await fetch('/user/1');
    const posts = await fetch(`/user/${user.id}/posts`);
    console.log('Данные пользователя:', user, posts);
  } catch (error) {
    console.error('Ошибка:', error);
  }
}
```
<br> Особенности async-функций
1. Всегда возвращают промис
2. Можно использовать `await` только внутри async-функций
3. Ошибки можно перехватывать с помощью `try/catch`
<br> Пример:
```
async function example() {
  return 42; // Эквивалентно return Promise.resolve(42)
}

example().then(console.log); // 42
```
## Fetch API
<br> Основы Fetch API
<br> Fetch API предоставляет современный интерфейс для HTTP-запросов, основанный на промисах.
<br>Базовый GET-запрос:
```
fetch('https://api.example.com/data')
  .then(response => {
    if (!response.ok) {
      throw new Error('Ошибка HTTP: ' + response.status);
    }
    return response.json();
  })
  .then(data => console.log(data))
  .catch(error => console.error('Ошибка:', error));
```
<br> Параметры запроса
```
fetch('https://api.example.com/data', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    'Authorization': 'Bearer token'
  },
  body: JSON.stringify({
    title: 'Новый пост',
    content: 'Содержание поста'
  }),
  mode: 'cors',
  credentials: 'include'
})
.then(response => response.json())
.then(data => console.log(data));
```
## Современный JavaScript (`ECMAScript`)
<br> История версий `ECMAScript`
1. ES3 (1999) - базовые возможности
2. ES5 (2009) - strict mode, JSON, методы массивов
3. ES6/ES2015 (2015) - классы, промисы, стрелочные функции, let/const
4. ES2016-ES2022 - ежегодные обновления с новыми возможностями
<br> Транспиляция с Babel
<br> Для поддержки старых браузеров современный код можно транспилировать в ES5:
```
// Исходный код (ES6+)
const square = num => num ** 2;
class User { constructor(name) { this.name = name; } }

// После транспиляции (ES5)
"use strict";

var square = function square(num) {
  return Math.pow(num, 2);
};

var User = function User(name) {
  this.name = name;
};
```
<br> Настройка Babel
1. Установка пакетов:
```
npm install --save-dev @babel/core @babel/cli @babel/preset-env
```
2. Конфигурационный файл `.babelrc`:
```
{
  "presets": [
    ["@babel/preset-env", {
      "targets": {
        "edge": "17",
        "firefox": "60",
        "chrome": "67",
        "safari": "11.1"
      }
    }]
  ]
}
```
## Сборка проектов (Bundlers)
<br> Зачем нужны сборщики
<br> Сборщики объединяют множество файлов в один или несколько бандлов, оптимизируют код и решают проблемы зависимостей.
<br> Популярные сборщики:
1. `Webpack`
2. `Rollup`
3. `Parcel`
4. `Vite`
<br> Пример с `Vite`
<br> Конфигурация `vite.config.js:`
```
export default {
  build: {
    outDir: './dist',
    emptyOutDir: true,
    rollupOptions: {
      input: {
        main: './src/main.js',
        admin: './src/admin.js'
      }
    }
  }
};
```
<br> После сборки получаем оптимизированные файлы:
```
dist/
  assets/
    index-abc123.js
    index-xyz456.css
  index.html
```
