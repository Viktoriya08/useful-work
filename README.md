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
