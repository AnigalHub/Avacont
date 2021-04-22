<template>
  <div id="app">
    <b-container fluid>
      <Navbar></Navbar>
      <Home></Home>
      <Features></Features>
      <Images></Images>
      <Catalog></Catalog>
      <Delivery></Delivery>
      <Portfolio></Portfolio>
     <!-- <feedback></feedback> -->
      <Contact></Contact>
      <Myfooter></Myfooter>
    </b-container>
  </div>
</template>

<script>

import Navbar from './components/navbar.vue'
import Home from "./components/home.vue";
import Features from "./components/features";
import Images from "./components/images";
import Catalog from "./components/catalog";
import Delivery from "./components/delivery";
import Portfolio from "./components/portfolio";
//import Feedback from "./components/feedback";
import Contact from "./components/contact";
import Myfooter from "./components/myfooter";

export default {
  name: 'App',
  components: {
      Myfooter,
      Contact,
     //Feedback,
      Portfolio,
      Delivery,
      Catalog,
      Images,
      Features,
      Navbar,
      Home
  }
}
</script>
<style>
  /*футер модального окна*/
  .modal-footer {display: none !important;}
  /*заголовок модального окна*/
  .modal-header{
    background: url("../public/images/background/background_4.jpg") 100% 100% no-repeat;
    background-size:100% 100%;
    filter: brightness(85%);
    padding: 0.5rem 1rem !important;
    text-decoration: underline;
  }
  /*фразы в заголовке модального меню*/
  .modal-title {
    font-weight: 800 !important;
    font-family: "Tenor Sans", sans-serif;
  }
  /*тело модального окна*/
  .modal-body{
    background: rgba(255, 244, 235, 0.55);
  }
  @media screen and (max-width: 500px) {
    /*"крестик" - кнопка закрытия модального окна*/
    .modal-header .close {
      padding: 0.5rem 0.5rem !important;
    }
  }
</style>

<style lang="scss">
  /*вся страница*/
  #app{
    height: 100%;
    margin: 0 !important;
    padding: 0 !important;
    background: url("../public/images/navbar.jpg") 100% 100%;
    filter: contrast(110%);
  }
  /*контейнер на блоки на всю площадь экрана*/
  .container-fluid{
    padding-left: 0 !important;
    padding-right: 0 !important;
  }
  /*контейнер на блоки посередине экрана*/
  .container{
    padding-right: 15px !important;
    padding-left: 15px !important;
  }
  /*контейнер, который включает в себя повтор блоков*/
  .flex-container {
    display: flex;
    flex-wrap: wrap;
  }
  /*параметры сетки бутстрап*/
  .row {margin: 0 !important;}
  /*затемнение компонентов*/
  .background{
    background-color: rgba(0, 0, 0, 0.48);
    padding: 1.5% 0;
  }
  /*заголовки*/
  h1{
    font-weight: 900 !important;
    font-family: "Playfair Display", serif;
    text-shadow: 2px 2px 2px #572e0c;
    color: #ffffff;
    padding-top: 5%;
    padding-bottom: 2%;
  }
  .h2_light{ /*светлый заголовок (когда фон темный)*/
    text-align: center;
    text-shadow: 2px 2px 2px #572e0c;
    color: #ffffff;
    padding: 1% 0;
  }
  h2,h3{font-family: "Playfair Display", serif;}
  h2{
    font-weight: 800 !important;
    text-align: center;
    text-shadow: 1px 1px 1px rgb(78, 43, 11,.6);
    color:  #4E2B0B;
    padding: 1% 0;
  }
  /*текст по всей странице*/
  .text,.text_light,table{font-size: 1.35rem;}
  /*текст на светлом фоне*/
  .text{
    font-weight: 500;
    text-shadow: 0.5px 0.5px 0.5px #5c4935;
    color: #6a4827;
  }
  /*текст на темном фоне*/
  .text_light{
    color: rgba(255, 255, 255, 0.85);
    font-weight: 600;
    text-shadow: 1.2px 1.2px 1.2px #49240c;
  }
  /*картинки на всем сайте*/
  img{
    width: 100%;
    height: auto;
  }
  /*таблица*/
  .table{
    text-align: center;
    border: 2px solid rgb(158, 118, 78, 0.55);
  }
  /*заголовок таблицы, ячейка таблицы*/
  .table th, .table td  {
    border: 1px solid rgb(158, 118, 78, 0.55) !important;
    padding: 0.5rem !important;
    display: table-cell;
    vertical-align: middle !important;
  }
  /*заголовок таблицы*/
  .table th{background: rgb(158, 118, 78, 0.55)  !important;}
  /*ячейка таблицы*/
  .table tr:not(:first-child):hover {background: rgba(160, 119, 79, 0.35) !important;}
  /*модальное окно (в компоненте "Каталог")*/
  .modal .row{
    padding-bottom: 2% !important;
    .col{ /*параметры сетки бутстрап (название накладки)*/
      display: flex;
      align-items: center;
    }
  }
  /*Компонент с названием и картинкой (самый первый)*/
  #Home{
    background: url("../public/images/background/background_1.jpg") 100% 100% no-repeat;
    background-size:100% 100%;
    #background{ background-color: rgba(0, 0, 0, 0.2);}/*затемнение компонента*/
    .text_light{ /*текст на темном фоне компонента*/
      font-weight: 400 !important;
      text-shadow: 1.2px 1.2px 1.2px #5f2c0c !important;
    }
    ul{padding-top: 4%;} /*список*/
    .col:first-child li{ /*элементы списка*/
      font-size: 1.4rem;
      padding-bottom: 5%;
      color: rgba(255, 255, 255, 0.9);
      list-style-image:url("../public/images/list.png");
      font-weight: 400;
      text-shadow: 0.5px 0.5px 0.5px #7c5639;
    }
  }
  /*Компонент "Преимущества"*/
  #Features{
    background: url("../public/images/background/background_2.jpg") 100% 100% no-repeat;
    background-size:100% 100%;
    padding-bottom: 5% !important;
    .part{border-bottom: 2px solid #7e4614;} /*блок с одной характеристикой (цифра, текст, картинки)*/
    .number{ /*цифры*/
      font-weight: 600;
      letter-spacing: 4px;
      font-family: 'Libre Caslon Display', serif;
      font-size: 4.5rem;
      color: #4f2f0d;
      text-shadow: 1px 1px 1px #ffffff;
    }
    .row:nth-child(3) .number_descr,.row:nth-child(4) .number_descr{line-height: 2rem;} /*фраза над цифрой*/
    .row:nth-child(4) .col-4  img{border-radius: 50%;}  /*картинки*/
    .row:nth-child(4) .col-4  img,.row:nth-child(5) .col-4 img{box-shadow: 2px 5px 5px #7c5639;} /*картинки*/
    .col,.col-2,.col-4{padding: 1.5% 0.6%;} /*параметры сетки бутстрап (цифры, текст, картинки)*/
    .col-2{/*параметры сетки бутстрап (блок с названием и цифрой)*/
      border-bottom: 2px solid #7e4614;
      text-align: center;
      font-weight: 700;
      line-height: 3rem !important;
      font-family: 'Playfair Display', serif;
      font-size: 1.5rem;
      text-shadow: .8px .8px .8px #7c644c;
      color: #4f2f0d;
    }
  }
  /*Компонент "5 картинок"*/
  #Images{
    .col{padding: 0 !important;} /*параметры сетки бутстрап (блоки под картинки)*/
    img{ /*картинки*/
      filter: brightness(55%);
      min-height: 65px;
      min-width: 72px;
      width: 100%;
      height: 100%;
    }
  }
  /*Компонент "Каталог"*/
  #Catalog{
    background: url("../public/images/background/background_2.jpg") 100% 100% no-repeat;
    background-size:100% 100%;
    padding-bottom: 2%;
    /*заголовки*/
    h2{padding-bottom: 0.2% !important;}
    h3{
      padding: 0.5% 0;
      color: #5a330c;
      font-weight: 800;
      letter-spacing: -1px;
    }
    h3,h4{text-align: center;}
    h4{
      font-weight: 500;
      text-shadow: 0.5px 0.5px 0.5px #7c644c;
      margin-bottom: 0 !important;
      line-height: 1.5rem;
      width: 80%;
      font-size: 1.4rem;
      color: black !important;
      height: 3.48rem !important;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 2% 1%;
      border-right:1.5px solid #7c644c;
    } /*название накладок*/
    .btn,h4{   /*кнопки и заголовки*/
      font-family: "Playfair Display", serif;
      float: left;
    }
    .btn{  /*кнопки*/
      background: rgba(255, 244, 235, 0.85);
      box-shadow: 2px 5px 5px #977f65;
      width: 100%;
      padding: 0 !important;
      &:hover { /*при наведении*/
        background: rgba(205, 147, 101, 0.15) !important;
        box-shadow: 2px 5px 5px #504436;
        border: none !important;
      }
      &:focus{background: rgba(199, 142, 96, 0.25) !important;} /*в фокусе*/
    }
    #more_details_svg{ /*svg в кнопке - (подробнее (вызов модального окна))*/
      width: 34px !important;
      height: 34px !important;
      margin-top: 3%;
    }
    img,.btn{box-shadow: 2px 5px 5px #977f65;} /*картинки и кнопки*/
    img{filter: contrast(115%) brightness(100%);} /*картинки*/
    .flex-container > div { /*блоки под каждый тип накладки*/
      width: 30%;
      margin: 0 1.5% 2% 1.5% !important;
      &:nth-child(4) {margin-left: 18% !important;}
    }
  }
  /*Компонент "Доставка"*/
  #Delivery{
    background: url("../public/images/background/background_4.jpg") 100% 100% no-repeat;
    background-size:100% 100%;
    h2{margin-top: 1.8%;} /*заголовок*/
    #map_svg{ /*svg-карта*/
      /*цвета и границы svg*/
      .st0{display:none;fill:#FFFFFF;stroke:#263E57;stroke-width:4;stroke-miterlimit:10;}
      .st1{fill: rgba(228, 191, 165, 0.72);stroke:#662A01;stroke-miterlimit:10;}
      .st2{fill:#613F29;}
      .st3{fill:none;stroke:#FFFFFF;stroke-width:1.3805;stroke-miterlimit:10;}
      .st4{fill:#FFFFFF;}
      .movement{animation: up-down-1 16s infinite;}
      .movement_2{animation: up-down-2 16s infinite;}
      .movement_3{animation: up-down-2 4s infinite;}
      @keyframes up-down-1{ /*главная метка*/
        0%{transform: initial;}
        25%{transform: translateY(7px);}
        50%{transform: initial;}
        100%{transform: translateY(-7px);}
      }
      @keyframes up-down-2{ /*остальные метки метка*/
        0%{transform: initial;}
        25%{transform: translateY(-7px);}
        50%{transform: initial;}
        100%{transform: translateY(7px);}
      }
    }
  }
  /*Компонент "Портфолио"*/
  #Portfolio{
    background: url("../public/images/background/background_2.jpg") 100% 100% no-repeat;
    background-size:100% 100%;
    .flex-container > img { /*блоки с картинками*/
      background: radial-gradient(70% 70%, #ffffff, rgb(210, 206, 211));
      width: 22%;
      height: 100%;
      margin: 0 1.5% 2.2% 1.5% !important;
      box-shadow: 2px 5px 5px #7c5639;
      &:hover{
        box-shadow: 2px 5px 5px #4b321f;
      }
    }
  }
  /*Компоненты - "Преимущества","Каталог","Портфолио"*/
  #Features, #Catalog, #Portfolio{padding: 1.8% 0;}
  /*Компонент "Обратная связь"*/
  #Feedback{
    background: url("../public/images/background/background_5.jpg") 100% 100% no-repeat;
    background-size:100% 100%;
    input{ /*поле ввода в форме заявки (фио, телефон, почта)*/
      padding: 25px 10px;
      min-height: 32px;
      margin-bottom: 1%;
    }
    input:hover, textarea:hover{box-shadow: 7px 7px 7px #161616;} /*наведение на любое поле ввода в форме заявки*/
    textarea{height: 87% !important;} /*поле ввода в форме заявки (текст)*/
    .col,.col-5{padding-bottom: 0.5%;} /*параметры сетки бутстрап*/
    button{ /*кнопка формы заявки*/
      display: block;
      margin: 0.5% auto 1% auto;
      padding: 0.25% 2%;
      font-weight: 600;
      font-family: "Tenor Sans", sans-serif;
      font-size: 1.1rem;
      border-width: 2px 0;
      border-style: solid none;
      border-color: #838383 #838383 #838383;
      border-radius: 6px;
      background: linear-gradient(rgba(188, 153, 122, 0.58), rgba(233, 223, 201, 0.76)) #eee4ce;
      transition: 0.2s;
      &:hover{background: linear-gradient(#eee0d7, #eee0d7) #d6c8bf;} /*при наведении*/
      &:active{background: linear-gradient(#b6a89f, #eee0d7) #d6c8bf;} /*в фокусе*/
    }
  }
  /*Компонент "Контакты"*/
  #Contact{
    background: url("../public/images/background/background_5.jpg") 100% 100% no-repeat; /*при добавлении заменить на background_2*/
    background-size:100% 100%;
    a { /*ссылки*/
      text-shadow: 0.025rem 0.025rem 0.025rem #7c644c;
      color: #6a4827;
      &:hover{
        text-shadow: 0.025rem 0.025rem 0.025rem #7c644c;
        color: #5a3827;
        text-decoration: none !important;
        font-weight: 700;
      }
    }
    .col-5 div{ /*блок под каждую информацию*/
      padding-bottom: 2%;
      background: white;
    }
    u{ /*название каждой информации*/
      font-size: 1.5rem;
      text-shadow: 0.025rem 0.025rem 0.025rem #7c644c;
      color: #40200b;
      font-weight: 600;
    }
    .address{ /*адрес*/
      padding: 4%;
      background: linear-gradient(to right top,rgba(131, 108, 84, 0.35),rgba(131, 108, 84, 0.15),rgba(131, 108, 84, 0.35));
      border-radius: 8px;
    }
    .map{ /*место под карту*/
      padding-top: 1%;
      iframe { /*карта с гугл-карт*/
        min-height: 460px;
        height: auto;
        width:100% !important;
        border:0;
        filter: brightness(95%);
      }
    }
  }


  /*********АДАПТИВНОСТЬ***********/

  @media screen and (max-width: 500px) {
    /*заголовки*/
    h1 {
      font-size: 1.5rem !important;
      text-align: center;
      padding-bottom: 0.5%;
    }
    h2, .h2_light {font-size: 1.25rem !important;}
    h3 {font-size: 1rem !important;}
    h4, h5 {
      font-size: 0.75rem !important;
      line-height: 0.9rem !important;
    }
    /*текст по всей странице*/
    .text, .text_light, table {font-size: 1rem;}
    /*заголовок таблицы, ячейка таблицы*/
    .table th, .table td {padding: 0.2rem !important;}
    /*Компонент с названием и картинкой (самый первый)*/
    #Home{
      img{width: 85% !important;} /*картинки*/
      .col:first-child li{ /*элементы списка*/
        font-size: 1rem !important;
        padding-bottom: 3% !important;
      }
    }
    /*Компонент "Преимущества"*/
    #Features {
      .number{ /*цифры*/
        font-size: 3.5rem !important;
        padding-top: 1.5%;
      }
      .text { /*текст на светлом фоне компонента*/
        line-height: 1rem;
        text-shadow: 0.1px 0.1px 0.1px #8f755b;
      }
      .part {
        flex-direction: column;
        padding-bottom: 2%;
        .col, .col-2, .col-4 {max-width: 100% !important;}  /*параметры сетки бутстрап (цифры, текст, картинки)*/
        .col-2 {border: none !important;} /*параметры сетки бутстрап (блок с названием и цифрой)*/
        .col {margin-top: -4% !important;}  /*параметры сетки бутстрап (текст)*/
        .col-4 {  /*параметры сетки бутстрап ( картинки)*/
          width: 70%;
          display: block;
          margin-left: auto !important;
          margin-right: auto !important;
        }
      }
      img {width: 90% !important;} /*картинки*/
    }
    /*Компонент "Каталог"*/
    #Catalog {
      .flex-container > div {/*блоки под каждый тип накладки*/
        width: 47%;
        display: block;
        margin-left: auto !important;
        margin-right: auto !important;
        margin-bottom: 5% !important;
        &:nth-child(4) {margin-left: auto !important;}
      }
      h4 {width: 80%;} /*название накладок*/
      .col {padding-right: 0 !important;}
      #more_details_svg{/*svg в кнопке - (подробнее (вызов модального окна))*/
        width: 22px !important;
        height: 30px !important;
        margin-top: 8.5%;
      }
    }
    /*Компонент "Доставка"*/
    #Delivery {
      .text_light {line-height: 1.2rem;}  /*текст на темном фоне компонента*/
    }
    /*Компонент "Обратная связь"*/
    #Feedback{
      background-size:cover;
      input{  /*поле ввода в форме заявки (фио, телефон, почта)*/
        padding: 2.5px 2.5px;
        min-height: 18px;
        height: 25px;
        background: rgba(255, 255, 255, 0.88);
      }
      .col-5{ /*параметры сетки бутстрап (место под форму)*/
        flex: 0 0 100% !important;
        max-width: 100% !important;
      }
      .col-5,.col{padding: 0 2px !important;} /*параметры сетки бутстрап*/
      button{ /*кнопка формы заявки*/
        margin-top: 3%;
        font-size: 1rem;
        margin-bottom: 4%;
      }
      .row{flex-direction: column} /*параметры сетки бутстрап*/
      textarea{ /*поле ввода в форме заявки (текст)*/
        height: 120px !important;
        background: rgba(255, 255, 255, 0.88);
      }
      form{padding: 0;} /*форма заявки*/
      label {margin-bottom: 0.25rem !important;} /*метка в форме заявки*/
    }
    /*Компонент "Контакты"*/
    #Contact{
      u {font-size: 0.9rem;} /*название каждой информации*/
      .col-5, .col {padding: 0 5px !important;} /*параметры сетки бутстрап*/
      .mail, .telephone {display: none;} /*почта и телефон*/
      .row { /*параметры сетки бутстрап*/
        flex-direction: column;
        .col-5 { /*параметры сетки бутстрап (место под информацию)*/
          max-width: 100% !important;
          margin-bottom: 2%;
        }
      }
      .col-5 div {padding-bottom: 0.2%;} /*блок под каждую информацию*/
      .text {line-height: 1.2rem;}   /*текст на светлом фоне компонента*/
      .map{ /*место под карту*/
        padding-top: 1%;
        iframe {min-height: 300px;} /*карта с гугл-карт*/
      }
      .address {padding: 1%;} /*адрес*/
    }
  }

  @media screen and (min-width: 500px)and (max-width: 768px) {
    /*заголовки*/
    h1{
      font-size: 1.7rem !important;
      text-align: center;
      padding-bottom: 0.5%;
    }
    h2,.h2_light{font-size: 1.25rem !important;}
    h3{font-size: 1.2rem !important;}
    h4,h5{
      font-size: 1rem !important;
      line-height: 1rem !important;
    }
    /*текст по всей странице*/
    .text,.text_light,table{font-size: 1.1rem;}
    /*Компонент "Каталог"*/
    #Catalog {
      .flex-container > div { /*блоки под каждый тип накладки*/
        width: 31.5%;
        margin: 0 0.8% 2% 0.8% !important;
      }
      h4 {width: 80%;} /*название накладок*/
      #more_details_svg{ /*svg в кнопке - (подробнее (вызов модального окна))*/
        width: 25px !important;
        height: 30px !important;
        margin-top: 8%;
      }
    }
    /*Компонент "Обратная связь"*/
    #Feedback{
      input{padding: 10px 5px;}  /*поле ввода в форме заявки (фио, телефон, почта)*/
      .col-5 {  /*параметры сетки бутстрап (место под форму)*/
        flex: 0 0 100% !important;
        max-width: 100% !important;
      }
      .col-5,.col{padding: 0 5px !important;}  /*параметры сетки бутстрап*/
      textarea{height: 120px !important;} /*поле ввода в форме заявки (текст)*/
      button{margin-top: 2%;} /*кнопка формы заявки*/
      form{padding: 0 10%;} /*форма заявки*/
      label {margin-bottom: 0.25rem !important;} /*метка в форме заявки*/
    }
    /*Компонент "Контакты"*/
    #Contact{
      u {font-size: 1.2rem;} /*название каждой информации*/
      .col-5,.col {padding: 0 5px !important;} /*параметры сетки бутстрап*/
      .mail, .telephone {display: none;} /*почта и телефон*/
      .row { /*параметры сетки бутстрап*/
        flex-direction: column;
        .col-5 { /*параметры сетки бутстрап (место под информацию)*/
          max-width: 100% !important;
          margin-bottom: 2%;
        }
      }
      .col-5 div {padding-bottom: 0.2%;} /*блок под каждую информацию*/
      .text {line-height: 1.4rem;}   /*текст на светлом фоне*/
      .map{ /*место под карту*/
        padding-top: 1%;
        iframe {min-height: 300px;}/*карта с гугл-карт*/
      }
      .address {padding: 1%;}/*адрес*/
    }
  }
  @media screen and (max-width: 768px) {
    /*Компонент с названием и картинкой (самый первый)*/
    #Home{
      background-size:cover;
      img{ /*картинки*/
        width: 80%;
        display: block;
        margin-left: auto;
        margin-right: auto
      }
      .row{ /*параметры сетки бутстрап*/
        flex-direction: column-reverse;
        .col:last-child{padding: 3%;} /*последний элемент*/
      }
      .col:first-child li{ /*элементы списка */
        font-size: 1.15rem;
        padding-bottom: 3.5%;
      }
      .carousel-indicators { /*индикаторы карусели*/
        display: none !important;
      }
    }
    /*Компонент "Преимущества"*/
    #Features{
      .number {font-size: 3rem;}  /*цифры*/
      .col-2 { /*параметры сетки бутстрап (блок с названием и цифрой)*/
        flex: 0 0 20% !important;
        max-width: 20% !important;
        font-size: 1.1rem;
        line-height: 2.5rem !important;
      }
      .col-2, .col{padding: 1.2% 0.6%;}  /*параметры сетки бутстрап (цифры, текст)*/
      .col-4 {  /*параметры сетки бутстрап (картинки)*/
        flex: 0 0 27% !important;
        max-width: 27% !important;
      }
      .text { /*текст на светлом фоне компонента*/
        line-height: 1.3rem;
        text-shadow: 0.1px 0.1px 0.1px #8f755b;
      }
    }
    /*Компонент "Доставка"*/
    #Delivery {
      .text_light {line-height: 1.4rem;}  /*текст на темном фоне компонента*/
      .col:first-child {  /*параметры сетки бутстрап (место под карту)*/
        display: block;
        margin-left: auto;
        margin-right: auto;
        max-width: 65%;
      }
      svg { /*svg-карта*/
        margin-top: -15%;
        padding-bottom: 5%;
      }
      .row {flex-direction: column-reverse;} /*параметры сетки бутстрап (карта и текст)*/
    }
    /*Компонент "Портфолио"*/
    #Portfolio {
      .flex-container > img { /*блоки с картинками*/
        background: radial-gradient(70% 70%, #ffffff, rgb(210, 206, 211));
        width: 30%;
        margin: 0 1.5% 2.2% 1.5% !important;
      }
    }
  }
  @media screen and (min-width: 768px)and (max-width: 992px) {
    /*заголовки*/
    h1{font-size: 2rem !important;}
    h2,.h2_light{font-size: 1.5rem !important;}
    h3{font-size: 1.25rem !important;}
    h4,h5{
      font-size: 1.05rem !important;
      line-height: 1rem !important;
    }
    /*текст по всей странице*/
    .text,.text_light,table{font-size: 1.1rem;}
    /*Компонент с названием и картинкой (самый первый)*/
    #Home{
      .col:first-child li{ /*элементы списка */
        font-size: 1.15rem;
        padding-bottom: 3.5%;
      }
    }
    /*Компонент "Преимущества"*/
    #Features {
      .number {font-size: 3.5rem;} /*цифры*/
      .col-2 { /*параметры сетки бутстрап (блок с названием и цифрой)*/
        font-size: 1.2rem;
        line-height: 2.5rem !important;
      }
      .col-2,.col {padding: 1% 0.6%;}  /*параметры сетки бутстрап (цифры, текст)*/
    }
    /*Компонент "Каталог"*/
    #Catalog{
      .flex-container > div { /*блоки под каждый тип накладки*/
        width: 31%;
        margin: 0 1% 2% 1% !important;
      }
      h4 {width: 84%;} /*название накладок*/
      #more_details_svg{  /*svg в кнопке - (подробнее (вызов модального окна))*/
        width: 30px !important;
        height: 30px !important;
        margin-top: 6%;
      }
    }
    /*Компонент "Обратная связь"*/
    #Feedback{
      input{padding: 20px 10px;} /*поле ввода в форме заявки (фио, телефон, почта)*/
    }
    /*Компонент "Контакты"*/
    #Contact{
      u{font-size: 1.15rem;} /*название каждой информации*/
    }
  }
  @media screen and (min-width: 992px)and (max-width: 1200px) {
    /*заголовки*/
    h1{font-size: 2.3rem !important;}
    h2,.h2_light{font-size: 1.75rem !important;}
    h3{font-size: 1.4rem !important;}
    h4,h5{font-size: 1.3rem !important;}
    /*текст по всей странице*/
    .text,.text_light,table{font-size: 1.2rem;}
    /*Компонент с названием и картинкой (самый первый)*/
    #Home{
      .col:first-child li{ /*элементы списка */
        font-size: 1.2rem;
        padding-bottom: 3.5%;
      }
    }
    /*Компонент "Преимущества"*/
    #Features {
      .number {font-size: 4rem;}  /*цифры*/
      .col-2 { /*параметры сетки бутстрап (блок с названием и цифрой)*/
        font-size: 1.4rem;
        line-height: 2.7rem !important;
      }
      .col-2,.col {padding: 1% 0.6%;} /*параметры сетки бутстрап (цифры, текст)*/
    }
    /*Компонент "Контакты"*/
    #Contact{
      u{font-size: 1.3rem;} /*название каждой информации*/
    }
  }
</style>
