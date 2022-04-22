# useful-work
# Показать/скрыть хедер при прокрутке страницы
 - https://github.com/vimp-dev/show-hide-header-by-scroll
 - https://www.youtube.com/watch?v=VayfnVMHknY&t=0s

# Покрасить карту Яндекс в темную тему
- https://www.youtube.com/watch?v=uOEakVEQlN4
- .ymaps-2-1-79-ground-pane {
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
