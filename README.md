# useful-work
# 1 Показать/скрыть хедер при прокрутке страницы
 - https://github.com/vimp-dev/show-hide-header-by-scroll
 - https://www.youtube.com/watch?v=VayfnVMHknY&t=0s

# 2 Покрасить карту Яндекс в темную тему
- https://www.youtube.com/watch?v=uOEakVEQlN4
- ```.ymaps-2-1-79-ground-pane {
        -ms-filter: grayscale(1);
       -webkit-filter: grayscale(1);
       -moz-filter: grayscale(1);
       -o-filter: grayscale(1);
       filter: grayscale(1);
     
   }

   .map::before {
       position: absolute;
       left: 0;
       top: 0;
       z-index: 100;
       background: #fff;
       display: block;
       width: 100%;
       height: 100%;
       mix-blend-mode: difference;
       pointer-events: none;
   }
# 3 Сетка
 - HTML
 ```
 <div class="b-net">
 <div class="b-net__col b-net__col-2 b-net__col-4"><div class="b"></div></div>
 <div class="b-net__col b-net__col-2 b-net__col-4"><div class="b"></div></div>
 <div class="b-net__col b-net__col-2 b-net__col-4"><div class="b"></div></div>
 <div class="b-net__col b-net__col-2 b-net__col-4"><div class="b"></div></div>
 </div>
 ```
 - CSS
 ```
 .b-net{
    display: flex;
        flex-wrap: wrap;
        justify-content: flex-start;
        margin-left: -5px;
        margin-right: -5px;
        & .b-net__col{
            width: 100%;
            padding: 0 5px;
            margin: 5px 0;
        }
        & .b-net__col-2{
            width: 50%;
        }
}
.b{
    background-color: rgb(95, 99, 160);
    height: 150px;
}

@media (min-width:768px) {
    .b-net{
        margin-left: -15px;
        margin-right: -15px;
        & .b-net__col{
            padding: 0 15px;
            width: 50%;
        }
        & .b-net__col-4{
            width: 33.33333%;
        }
    }
}
@media (min-width:1250px) {
    .b-net{
        & .b-net__col{
            margin: 5px 0;
        }
        & .b-net__col-4{
            width: 25%;
        }
    }
}
```
 # 4 Акордеон на CSS (details, summary)  
 https://xhtml.ru/2020/html/details-summary-accordion/
 # 5 Аккордеон на JS
 https://myrusakov.ru/js-accordion.html
 # 6 Выбор языка на сайте
 ```
 <select name="" id="input0" required="required" style="background-image:url(images/lng_ru.png);">
    <option  style="background-image:url(images/lng_ru.png);" value="rus">rus</option>
    <option  style="background-image:url(images/lng_eng.png);" value="eng">eng</option>
</select>
<script>
$('#input0').click(function() {
 if($("select#input0 :selected").val() == "rus") {
    $("select#input0").attr('style', 'background-image:url(images/lng_ru.png);');
 }
 if($("select#input0 :selected").val() == "eng") {
    $("select#input0").attr('style', 'background-image:url(images/lng_eng.png);');
 }
    console.log('select color: '+$("select#input0 :selected").val());
});
</script>
```
# 7 Функция на addEventListener
```
const searchCategoryBtn = document.querySelector('.search-catalog__btn');

searchCategoryBtn.addEventListener('click', function(){
    this.classList.toggle('open');
    this.nextElementSibling.classList.toggle('open');

});
```
# 8 Библиотека для картинок галерея, аля fancybox на чистом js
https://biati-digital.github.io/glightbox/#specifications
# 9 Плагин - кастомный скролл-бар
https://www.npmjs.com/package/simplebar
# 10 Кнопка прокрутки вверх
```
<button class="b-btn-up"></button>
.b-btn-up{
    position: fixed;
    bottom: 20px;
    right: 15%;
    z-index: 100;
    width: 50px;
    height: 50px;
    border: none;
    border-radius: 50%;
    background-image: url(../images/arrow-white.svg);
    background-position: center center;
    background-repeat: no-repeat;
    background-size: auto;
    background-color: #7ac751;
    transform: rotate(-90deg);
    opacity: 0;
    visibility: hidden;
    transition-property: opacity;
    transition-duration: 1s;
    &.js-visible{
        opacity: 1;
        visibility: visible;
    }
}

const goTopBtn = document.querySelector('.b-btn-up');

(function() {
    'use strict';
  
    function trackScroll() {
      const scrolled = window.pageYOffset;
      const coords = document.documentElement.clientHeight;
  
      if (scrolled > coords) {
        goTopBtn.classList.add('js-visible');
      }
      if (scrolled < coords) {
        goTopBtn.classList.remove('js-visible');
      }
    }
  
    function backToTop() {
      if (window.pageYOffset > 0) {
        window.scrollTo(0,0);
      }
    }
  
    window.addEventListener('scroll', trackScroll);
    goTopBtn.addEventListener('click', backToTop);
  })();
  ```
  # 11 Фрилансер по жизни
  https://fls.guru/cssanimation.html
  # 12 Кастомизация select
  https://github.com/jshjohnson/Choices - библиотека choices.js
  https://www.youtube.com/watch?v=dnC7XCYb9Qg - видео описание
  # 13 Кастомный ползунок для фильтра цен
  https://refreshless.com/nouislider/ - noUiSlider
  # 14 Плавное появление элемента
  ```
  .element{
    transform: scale(0);
    trensition: transform 0.5s ease 0.0s;
   }
   .element:hover{
   transform: scale(1)
   }
   ```
   # 15 Отключить на Slick JQ десктопе
   mobileFirst: true,
   settings: 'unslick',
   ```
   $(".header__cats-slider").slick({
        slidesToShow: 5,
        arrows: true,
        infinite: false,
        mobileFirst: true,
        responsive: [
          {
            breakpoint: 1300,
            settings: 'unslick',
          },
          {
            breakpoint: 992,
            settings: {
              slidesToShow: 4,
            },
          },
          {
            breakpoint: 670,
            settings: {
              slidesToShow: 2,
            },
          }
        ]
    });
   ```
# 16 экранная типографика - убрать висячие предлоги 
         https://www.artlebedev.ru/typograf/about/
    
# 17 Предотвратите скрытие содержимого под фиксированным заголовком с помощьюscroll-margin-top
    https://www.bram.us/2020/03/01/prevent-content-from-being-hidden-underneath-a-fixed-header-by-using-scroll-margin-top/
    
# 18 Ползунки для фильтра - плагин js
    https://www.youtube.com/watch?v=kWoAKq7N2Ew
    https://refreshless.com/nouislider/slider-options/
    
 # 19 Для пейджспида - разгон сайта
    https://thanosjs.org/
    
 # 20 Кастомизация input checkbox
    https://itchief.ru/html-and-css/styling-checkbox-and-radio
 # 21 Счетчик списка на CSS 
    https://russianblogs.com/article/8486683955/
 # 22 Повесить обработчик клик на родительский блок и внем потом искать кнопку (если кнопок много, то это сократит обработчик до одного, всето того, чтобы вешать обработчик на каждую кнопку)
    ```
    <div class="parent">
    <button class="button">Кнопка</button>
    <button class="button">Кнопка</button>
    <button class="button">Кнопка</button>
    <button class="button">Кнопка</button>
    </div>
    
    const parent = document.querySelector(".parent");
    
    function showConsole(){
      console.log("Ура");
    }
    
    parent.addEventListener("click", function (event){
     if(event.target.closest('.button')){   // event.target.closest - проверяет наличие класса button
      showConsole();
     }
     });
     ```
 # 23 посмотреть все аргументы, которые передаются в функцию
     ```
     function showSumAll(){
       console.log(arguments);
     }
     showSumAll(2, 3, 5);
     ```
     Превратить аргументы в массив и работать уже с массивом в функции
     ```
     function showSumAll(...arg){
       console.log(arg);
       let sum = arg.reduce((accum, item) => accum += item);
       console.log(sum);
     }
     showSumAll(2, 3, 5);
     ```
 # 24 Интерполяция строк `${randInt(0, 255)} `
     ```
     function randInt(min, max){
      let rand = min + Math.random() * (max + 1 - min);
      return Math.floor(rand);
     }

     block2.addEventListener('click', ()=>{
         block2.style.background = `rgb(${randInt(0, 255)},${randInt(0, 255)},${randInt(0, 255)})`;
     })
     ```
 # 25 форматирование цифровых значений new Intl.NumberFormat("ru");
     
     const formatter = new Intl.NumberFormat("ru");
     переменная.innerText = formatter.format(значение-цифра);
     
 # 26 Отмена всплытия события - event.stopPropagation
     https://www.youtube.com/watch?v=GsYiq4Ic384&t=9s
     
 # 27 Анимация
     https://projects.verou.me/animatable/
     
 # 28 Палигон
     https://bennettfeely.com/clippy/
     
 # 29 Бэкграунд цветом и градиентом
     background: radial-gradient(40.63% 46.8% at 68.26% 65.2%, rgba(195, 147, 103, 0.7) 0%, rgba(195, 147, 103, 0) 100%), #E04E39;
     
  # 30 Переносы длинных слов HTML
     https://www.tune-it.ru/web/leksa/blog/-/blogs/ukrosaem-dlinnyj-tekst-sredstvami-html-i-css
     
  # 31 Кодировка SVG для CSS
     https://yoksel.github.io/url-encoder/ru/
     
  # 32 Перекрасить svg
     filter: drop-shadow(0px 5px 24px rgba(226, 64, 55, 0.35))
     
     svg
        stroke: $blue-light
        filter: drop-shadow(1px 1px 1px rgba(0,0,0,0.0))
        transition: filter .3s
     &:hover
         svg
             filter: drop-shadow(1px 1px 1px rgba(0,0,0,0.3))
     
 # 33 Удалить ветку в гите (если ее нет локально, а только на гите)
     git push -d origin new_templates
     https://stackoverflow.com/questions/2003505/how-do-i-delete-a-git-branch-locally-and-remotely
     
 # 33 Плавное раскрытие текстового блока
     На текстовый блок вешаем data-cut-text со значением, которое будет соответсвовать значению кнопки data-cut
     
     .block-text
      Много текста одним параграфом
      
      
     .block-text
            overflow: hidden
            display: -webkit-box
            -webkit-line-clamp: 6
            -webkit-box-orient: vertical
            max-height: 135px
            height: auto
            transition: all 0.5s ease-out
            &.open
                -webkit-line-clamp: 50
                max-height: 600px
                transition: all 0.5s ease-in
                
     JS
    function cutText(textBlock) {
    const textBlocks = document.querySelectorAll("[data-cut-text]")
    const btns = document.querySelectorAll("[data-cut]")

    if (textBlocks || btns) {
        btns.forEach(btn =>{
            btn.addEventListener('click', ()=>{

                textBlocks.forEach(block =>{

                    if(block.dataset.cutText == btn.dataset.cut){
                        block.classList.toggle('open')
                        //block.style.height = `${block.scrollHeight}px`
                        btn.classList.toggle('open')
                    }
                })

                 if(btn.classList.contains('open')){
                     btn.innerHTML = 'Свернуть'
                 } else{
                     btn.innerHTML = 'Развернуть'
                 }
                  })
              })
          }

      }
      
# 34 Бурген анимация на svg
      https://codepen.io/kevinpowell/pen/gOKpOyy
      
# 35 CSS свойство, которое сообщает браузеру какие элементы меняются, трасформируются на странице и им надо больше аппаратных ресурсов. Чтобы анимация не тормозила, на элементы добавляем это свойство  -  will-change: transform;
      
      transform - указываем то свойств, которое меняется при анимации
      
     	``` 
     	.content, .hero, .main-header, .gallery > * {
		will-change: transform;
	}
	```

# 36 Подбор фона под картинку
https://github.com/fast-average-color/fast-average-color

# 37 Направление Transform CSS
transform-origin: center left

# 38 Автоматический перенос грид-элементов

Чтобы колонки переносились можно использовать auto-fit или auto-fill. grid-template-columns: repeat( auto-fit, minmax(250px, 1fr) ); 
Эти ключевые слова говорят браузеру перенести элемент на новую строку, если не хватает ширины, чтобы его вместить без перекрытия.

# 39 Работа с SVG

HTML
svg(width="100px" height="100px" viewBox="0 0 100 100" data-max-value="100" data-current-value="27").circle
  circle(cx="50" cy="50" fill="none" r="47" stroke-width="3" 	stroke-linecap='round' stroke="#c7c7c7")
  circle(id="circle-progress" cx="50" cy="50" fill="none" r="47" stroke-width="3" 	stroke-linecap='round' stroke="#b5a053" stroke-dasharray="295 295" stroke-dashoffset="50")
  
 CSS
 .circle {
  width: 92px;
  height: 92px;
  margin: 33px;
  transform: rotate(-90deg)
}

JS
const circle = document.getElementById('circle-progress');
const maxValue = parseInt(circle.parentElement.dataset.maxValue);
const currentValue = parseInt(circle.parentElement.dataset.currentValue);

const percentValue = (currentValue / maxValue) * 100;
const circleLength = 2 * Math.PI * parseFloat(circle.getAttribute('r'));
const dashOffset = circleLength - (percentValue / 100) * circleLength;

circle.setAttribute('stroke-dasharray', circleLength);
circle.setAttribute('stroke-dashoffset', dashOffset);
