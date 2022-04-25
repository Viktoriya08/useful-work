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
