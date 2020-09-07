<template>
  <div id="app">
    <b-container fluid>
      <Navbar></Navbar>
      <Home></Home>
      <feature></feature>
      <images></images>
      <catalog></catalog>
      <delivery></delivery>
      <portfolio></portfolio>
      <feedback></feedback>
      <contact></contact>
     <myfooter></myfooter>
    </b-container>
  </div>
</template>

<script>

import Navbar from './components/navbar.vue'
import Home from "./components/home.vue";
import Feature from "./components/feature";
import Images from "./components/images";
import Catalog from "./components/catalog";
import Delivery from "./components/delivery";
import Portfolio from "./components/portfolio";
import Feedback from "./components/feedback";
import Contact from "./components/contact";
import Myfooter from "./components/myfooter";

export default {
  name: 'App',
  components: {
      Myfooter,
      Contact,
      Feedback,
      Portfolio,
      Delivery,
      Catalog,
      Images,
      Feature,
      Navbar,
      Home
  }
}
</script>

<style lang="scss">
  #app{
    height: 100%;
    margin: 0 !important;
    padding: 0 !important;
    background: url("assets/images/navbar.jpg") 100% 100%;
  }
  .container-fluid{
    padding-left: 0 !important;
    padding-right: 0 !important;
  }
  .row {
    margin: 0 !important;
  }
  h1{
    font-weight: 900;
    font-family: 'Tenor Sans', sans-serif;
    text-shadow: 2px 2px 2px #572e0c;
    color: #ffffff;
    padding-top: 5%;
    padding-bottom: 2%;
  }
  .h2_light{
    font-weight: 800;
    text-align: center;
    font-family: 'Tenor Sans', sans-serif;
    text-shadow: 2px 2px 2px #572e0c;
    color: #ffffff;
    padding: 1% 0;
  }
  h2{
    font-weight: 800 !important;
    text-align: center;
    font-family: 'Tenor Sans', sans-serif;
    text-shadow: 1px 1px 1px rgba(255, 255, 255, 0.74);
    color:  #4E2B0B;
    padding: 1% 0;
  }
  .text{
    font-weight: 500;
    text-shadow: 0.5px 0.5px 0.5px #80674e;
    color: #6a4827;
  }
  .text_light{
    color: rgba(255, 255, 255, 0.85);
    font-weight: 600;
    font-family: "Tenor Sans", sans-serif;
    text-shadow: 1.2px 1.2px 1.2px #49240c;
  }
  .text,.text_light{
    font-size: 1.35rem;
  }
  #feature, #catalog,
  #portfolio,
  #contact{
    padding: 1.5% 0;
  }
  img{
    width: 100%;
  }
  .background{
    background-color: rgba(0, 0, 0, 0.48);
    padding: 1.5% 0;
  }
  @media screen and (max-width: 500px) {
    h1{
      font-size: 1.5rem !important;
      text-align: center;
      padding-bottom: 0.5%;
    }
    h2,.h2_light{
      font-size: 1.25rem !important;
    }
    h3{
      font-size: 1rem !important;
    }
    h4{
      font-size: 0.9rem !important;
      line-height: 0.7rem !important;
    }
    .text,.text_light{
      font-size: 0.9rem;
    }
  }
  @media screen and (min-width: 500px)and (max-width: 768px) {
    h1{
      font-size: 1.7rem !important;
      text-align: center;
      padding-bottom: 0.5%;
    }
    h2,.h2_light{
      font-size: 1.25rem !important;
    }
    h3{
      font-size: 1.2rem !important;
    }
    h4{
      font-size: 1.1rem !important;
    }
    .text,.text_light{
      font-size: 1rem;
    }
  }
  @media screen and (min-width: 768px)and (max-width: 992px) {
    h1{
      font-size: 2rem !important;
    }
    h2,.h2_light{
      font-size: 1.5rem !important;
    }
    h3{
      font-size: 1.25rem !important;
    }
    h4{
      font-size: 1.2rem !important;
    }
    .text,.text_light{
      font-size: 1rem;
    }
  }
  @media screen and (min-width: 992px)and (max-width: 1200px) {
    h1{
      font-size: 2.3rem !important;
    }
    h2,.h2_light{
      font-size: 1.75rem !important;
    }
    h3{
      font-size: 1.4rem !important;
    }
    h4{
      font-size: 1.3rem !important;
    }
    .text,.text_light{
      font-size: 1.2rem;
    }
  }
</style>
