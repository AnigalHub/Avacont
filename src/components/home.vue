<template>
    <div id="home">
        <div id="background">
            <b-container>
                <h1>Накладки на бревно и блок-хаус</h1>
                <b-row>
                    <b-col>
                        <div class="text_light">
                            Изготовление накладок из дерева под розетки,
                            выключатели, радиаторы, светильники и карнизы
                            разных производителей.
                        </div>
                        <ul>
                            <li v-for="(feature,index) in Features" :key="index">{{feature}}</li>
                        </ul>
                    </b-col>
                    <b-col>
                        <b-carousel
                                id="carousel-fade" fade indicators>
                            <b-carousel-slide>
                                <template v-slot:img>
                                    <img src="../../public/images/home/double_pad.jpg"/>
                                </template>
                            </b-carousel-slide>
                            <b-carousel-slide>
                                <template v-slot:img>
                                    <img src="../../public/images/home/log_pad.jpg"/>
                                </template>
                            </b-carousel-slide>
                            <b-carousel-slide>
                                <template v-slot:img>
                                    <img src="../../public/images/home/pad_on_switch.jpg"/>
                                </template>
                            </b-carousel-slide>
                            <b-carousel-slide>
                                <template v-slot:img>
                                    <img src="../../public/images/home/triple_pad.jpg"/>
                                </template>
                            </b-carousel-slide>
                        </b-carousel>
                    </b-col>
                </b-row>
            </b-container>
        </div>
    </div>
</template>

<script>
    export default {
        name: "home",
        data(){
            return{
                Features:[
                    'Изготовление от 2 до 10 дней',
                    'Огромный ассортимент',
                    'Гарантия от 12 месяцев',
                    'Быстрый монтаж',
                    'Долговечность',
                ]
            }
        }
    }
</script>

<style>
    @media screen and (max-width: 768px) {
        .carousel-indicators {
            display: none !important;
        }
    }
</style>
<style scoped lang="scss">
    #background{
        background-color: rgba(0, 0, 0, 0.2);
    }
    #home{
        background: url("../../public/images/background/background_1.jpg") 100% 100% no-repeat;
        background-size:100% 100%;
    }
    ul{
        padding-top: 4%;
    }
    .text_light{
        font-weight: 500 !important;
    }
    li{
        font-size: 1.5rem;
        padding-bottom: 5%;
        color: rgba(255, 255, 255, 0.9);
        list-style-image:url("../../public/images/list.png");
        font-weight: 600;
        font-family: 'Tenor Sans', sans-serif;
        text-shadow: 0.5px 0.5px 0.5px #7c5639;
    }

    @media screen and (max-width: 500px) {
        li{
            font-size: 1rem !important;
            padding-bottom: 3% !important;
        }
        img{
            width: 85% !important;
        }
    }
    @media screen and (max-width: 768px) {
        #home{
            background-size:cover;
        }
        img{
            width: 80%;
            display: block;
            margin-left: auto;
            margin-right: auto
        }
        .row{
            flex-direction: column-reverse;
            .col:last-child{
                padding: 3%;
            }
        }
        li{
            font-size: 1.15rem;
            padding-bottom: 3.5%;
        }
    }
    @media screen and (min-width: 768px)and (max-width: 992px) {
        li{
            font-size: 1.15rem;
            padding-bottom: 3.5%;
        }
    }
    @media screen and (min-width: 992px)and (max-width: 1200px) {
        li{
            font-size: 1.2rem;
            padding-bottom: 3.5%;
        }
    }


</style>