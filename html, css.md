Основные теги
<section> ... </section>   <!-- создание секций и разделов -->
<footer> ... </footer>     <!-- подвал страницы -->
<html lang="ru">   <!-- lang — атрибут тега <html>, указывает язык сайта -->
<link rel="stylesheet" href="styles/style.css" />  <!-- подключение CSS-файла -->

<p>Это <span class="highlight">важное слово</span> в предложении.</p>  <!--строчный контейнер без собственного оформления,
используется для выделения части текста или небольшого фрагмента внутри других элементов-->

<img class="card-image"
     src="https://code.s3.yandex.net/web-code/images/freetrack/04/card-2.jpg"
alt="Разметка теннисного корта крупным планом" /> <!-- картинка и текст при её отсутствии -->

<section class="section about" id="about"></section>    <!--id — уникальный идентификатор элемента,
нужен для создания якорных ссылок и навигации-->
<a href="#about">Что это</a> <!-- ссылка на элемент на той же странице -->
<a href="https://site.com/page#section">Ссылка с другой страницы</a>
html {
  scroll-behavior: smooth; /* плавная прокрутка к якорю */
}
#part-11 {
  color: #ff0000;
}

<!-- Независимый контент -->
<article>
  <h2>Кусочек мотивации</h2>
  <ul>
    <li>Вы отлично справляетесь!</li>
    <li>Впереди ещё много интересного!</li>
    <li>Не сдавайтесь!</li>
  </ul>
</article>
<!-- article — для независимого блока, который можно вынести со страницы без потери смысла -->

<!-- Цитаты -->
<blockquote cite="https://praktikum.yandex.ru">
  Достаточно начать — и, конечно, не бросить. 
  Мы поможем приступить к учёбе и справиться с трудностями.
</blockquote>
<!-- blockquote — для цитат; по умолчанию имеет левый отступ -->
<!-- cite  — указать автора цитаты -->
<p>Как сказал преподаватель: <q>Практика — лучший способ учиться</q>.</p>
<!-- q — строчная цитата, автоматически оформляется в кавычки (в русском — «ёлочки») -->

Маркерованный список
<ul>                   /* создать список */
  <li>хитон;</li>      /* элементы */
  <li>фибула;</li>
  <li>пояс (даже два).</li>
</ul>
Нумерованный список
<ol>                  /* создать список */
    <li>Учение Сократа и сократические школы.</li>    /* элементы */
    <li>Платон и его Академия.</li>
    <li>Учение Аристотеля.</li>
</ol> 
<!-- Управление маркерами списков -->
ul {
  list-style: none; /* убирает маркеры списка */
  /* list-style можно использовать для изменения формы, позиции или изображения маркера */
}

Таблица(html)
<table>
  <caption>Результаты опроса студентов</caption> <!--  что за данные представлены в таблице, идёт сразу после <table> -->
  <thead>  <!-- строка(и) с заголовками столбцов, перед tbody и tfoot -->
    <tr>
      <th>Заголовок 1</th>
      <th>Заголовок 2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Данные 1</td>
      <td>Данные 2</td>
    </tr>
  </tbody>
</table>
<!-- 
<tr> и <table> — только для структуры, а содержимое располагается внутри <td> и <th>
Ячейки могут объединяться: rowspan — по вертикали, colspan — по горизонтали
<thead> — семантический блок заголовков таблицы, похож на <header>
-->

Таблица(scc)
td,
th {
  border: 1px solid #000; /* рамки ячеек */
}
table {
  border-collapse: collapse; /* убирает промежутки между рамками ячеек, делая таблицу цельной */
}

Комментарии
<!-- Это комментарий в HTML -->
/* Это комментарий в CSS */

Общие правила
* {
  box-sizing: border-box; /* включает padding и border в общую ширину элемента */
}

Границы
border-color: #000;      /* цвет границы */
border-width: 1px;       /* толщина границы */
border-style: solid;     /* тип границы: solid, dashed, dotted, double */
border: 3px solid #000;  /* сокращённая запись: толщина, тип, цвет */

Отступы
margin: 0 auto;          /* центрирует элемент по горизонтали */
margin: 20px;            /* внешний отступ */
padding: 10px;           /* внутренний отступ */
padding: 25px 25px 30px 25px;  /* сверху, справа, снизу, слева */

Размеры и позиционирование
width: 100%;
height: 100%;            /* занимает всю ширину/высоту родителя */
position: relative;       /* создаёт точку отсчёта для absolute */
display: block;           /* блочный элемент */
display: inline;          /* строчный элемент */
display: inline-block;    /* блочно-строчный элемент */

Гибкая верстка (Flexbox)
display: flex;            /* включает flex-контейнер */
flex-direction: row;      /* горизонтально (по умолчанию) */
flex-direction: column;   /* вертикально */
justify-content: flex-start;  /* выравнивание по горизонтали */
align-items: flex-start;      /* выравнивание по вертикали */
align-items: end;             /* прижать элементы к низу */

Сетка (Grid)
display: grid;                       /* используем сетку */
grid-template-columns: 711px 399px;  /* ширина колонок */
grid-template-areas: "result details"; /* имена областей */
grid-area: result;                   /* привязка элемента к области */
gap: 30px;                           /* расстояние между ячейками */

Фон и изображения
background-color: #fff;                      /* цвет фона */
background-image: url("ссылка");             /* картинка фона */
background-size: cover;                      /* заполнить весь блок */
background-size: contain;                    /* уместить всю картинку */
background-size: 220px 400px;                /* точные размеры */
background-repeat: no-repeat;                /* не повторять фон */
background-repeat: repeat-y;                 /* повтор по вертикали */
background-position: center;                 /* по центру */
background-position: right bottom;           /* справа снизу */
background-position: 150px 50px;             /* отступы от угла */
object-fit: cover;                           /* заполняет контейнер */

Текст и шрифт
color: #000;                        /* цвет текста */
font-size: 16px;                    /* размер шрифта */
font-family: 'Open Sans', 'Arial', sans-serif;  /* шрифт */
font-family: serif;                 /* с засечками */
font-family: sans-serif;            /* без засечек */
font-family: monospace;             /* равная ширина символов (для кода) */
font-family: cursive;               /* рукописный, наклонный */
font-family: fantasy;               /* декоративный */
font-family: system-ui;             /* шрифт операционной системы по умолчанию
font-weight: 700;                   /* толщина (например, bold) */
font-style: italic;                 /* курсив */
text-align: center;                 /* выравнивание текста */
letter-spacing: 0;                  /* расстояние между буквами */
text-transform: uppercase;          /* все буквы — заглавные */
text-decoration: underline;         /* подчеркнутый текст */
text-decoration: line-through;      /* зачеркнутый текст */
Декларация шрифта:
@font-face {                        /* cообщает браузеру, где взять шрифт и как его назвать */
  src: url("путь к файлу");
  font-family: 'Best Font Ever'; /* имя шрифта */
}
Применение шрифта:
div {
  font-family: 'Best Font Ever', 'Arial', 'Helvetica', sans-serif;  /* Альтернативные шрифты (Arial, Helvetica, sans-serif) указывают на случай, если основной шрифт не загрузится*/
  font-weight: bold;
  font-style: italic;
}
Поддержка разных форматов:
@font-face {
    src: url(путь к файлу.woff2) format('woff2'),
             url(путь к файлу.woff) format('woff'),
             url(путь к файлу.ttf) format('truetype'),
             url(путь к файлу.eot) format('eot');
} 
/*Чтобы использовать локальный шрифт, добавляют функцию local() в src */
Загрузка шрифтов и свойство font-display
@font-face {
  src: url('./Inter-regular.woff') format('woff');
  font-family: 'Inter';
  font-display: swap; /* сначала альтернативный шрифт, затем заменяет на Inter */
}
*/block — текст будет прозрачным до полной загрузки шрифта; */
*/swap — сначала показывается альтернативный шрифт, затем заменяется на нужный. */
Оформление текста: text-transform
h1, button {
  text-transform: uppercase; 
}
*/uppercase — сделать все буквы заглавными;*/
*/lowercase — сделать все буквы строчными;*/
*/capitalize — все первые буквы в словах сделать заглавными*/

p {
  letter-spacing: 2px;  /* межбуквенное расстояние в пикселях */
  line-height: 1.5;     /* межстрочное расстояние как доля размера шрифта */
}
/*line-height - относительные значения считаются от размера шрифта (1 = размер шрифта, 1.5 = полуторная высота строки)*/

text-decoration: none - /*убирает любые декоративные линии*/
text-decoration: underline  - /*подчёркивание текста*/

Тени
box-shadow: -2px 2px 5px #FD6969;   /* тень элемента */
text-shadow: 1px 1px 3px #888;      /* тень текста */

Цвет и прозрачность
background-color: rgb(115 170 200 / 0.5); /* полупрозрачный цвет (50%) */
