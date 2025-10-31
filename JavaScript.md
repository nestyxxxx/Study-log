console.log  вывести информацию в браузерную консоль
alert();  можно вывести сообщение на страницу(строки)
Сложение строк называют «конкатенацией»
let pages;  создали коробку с именем pages, то есть «страницы» 
<script src="script.js"></script> подключение js (пишут перед </body>)
let aliExpress = ['Лазерная указка Xiaomi', 'Гарнитура в виде телефонной трубки', 'Форма для льда «Титаник»']; массив
console.log(aliExpress[1]); // "Гарнитура в виде телефонной трубки"  элемент массива
let randomNumber = Math.random(); рандомное число от 0 до 1 
Math.random() * 10 от 0 до 10
Math.floor() округлить до целого числа вниз
let randomNumberInt = Math.floor(Math.random() * 10); вместе
length длина массива  
console.log(aliExpress.length)  покажет длину массива
function sayHello() {
  alert('Привет, Андрей'); // тело функции
}
sayHello();  Привет, Андрей 
document  вся информация о веб-странице, доступ к управлению любым элементом на странице
let photoElement = document.querySelector('.photo');    доступ к инструментам осуществляется через символ точки, инструмент querySelector нашёл на странице нужный элемент

let button = document.querySelector('.button');     находим элемент .button и кладём в переменную
button.addEventListener('click', function () {    обращаемся к переменной, добавляем элементу слушатель клика
   что происходит при клике по кнопке
}); 
textContent   для чтения или изменения текста внутри HTML-элемента

if (надпись длиннее 40 символов) {
    уменьшить размер надписи до 33px
} else {
    установить обычный размер в 42px   
}  
phrase.style.fontSize = '42px';

let user = {                   объекты
    name: 'Мария',
    dotaLevel: 21,
    dogName: 'Железногорск'
};

let image = document.querySelector('.image');
console.log(image.src); // https://...адрес картинки
image.src = 'https://images.unsplash.com/photo-1548104210-6d130801c54a';      поменяли картинку

let image = document.querySelector('.image');

let object = {
    name: 'Proctrastination street', // свойство с именем
    link: 'https://images.unsplash.com/photo-1548104210-6d130801c54a'    свойство с адресом
};
image.src = object.link;     свойству src объекта image присвоили значение свойства link объекта object

<!-- подключим библиотеку -->
<script src="https://library-website.com/lib.js"></script>

let array = ['животные', 'растения', 'грибы', 'микроорганизмы', 'вирусы'];    массив
for (let i = 0; i <= 4; i+=1) {    (начальное значение переменной-счётчика; ограничение; шаг)
  console.log(array[i]);
}
закончила блок
