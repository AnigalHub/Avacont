<template>
    <div id="feature">
        <b-container>
            <h2>Характеристики изделий</h2>
            <b-row class="part" v-for="(catalog, index) in calalog" :key="index">
                <b-col cols="2">
                    <div class="number_descr">{{catalog.number_descr_2}}</div>
                    <div class="number">{{catalog.number}}</div>
                    <div class="number_descr">{{catalog.number_descr}}</div>
                </b-col>
                <b-col class="text">
                    {{catalog.descr}}
                </b-col>
                <b-col cols="4">
                    <b-row>
                        <b-col  v-for="(value, index) in catalog.img" :key="index">
                            <img :src="value.src" :alt="value.alt"/>
                        </b-col>
                    </b-row>
                </b-col>
            </b-row>
          <!--  <b-row class="part">
                <b-col cols="2">
                    Более
                    <div class="number">30</div>
                    позиций
                </b-col>
                <b-col class="text">
                    Мы изготавливаем более 30 видов деревянных накладок, и продолжаем разрабатывать новые дизайны и функциональность изделий!
                </b-col>
                <b-col cols="4">
                    <b-row>
                        <b-col>
                            <img src="../assets/images/12.jpg"/>
                        </b-col>
                        <b-col>
                            <img src="../assets/images/11.jpg"/>
                        </b-col>
                    </b-row>
                </b-col>
            </b-row>
            <b-row class="part">
                <b-col cols="2">
                    <div class="number">8</div>
                    Диаметров бревна
                </b-col>
                <b-col class="text">
                    Мы разработали изделия для 8 самых распространенных размеров бревен. Если у Вас нестандартное бревно, то пишите - мы обязательно что-нибудь придумаем!
                </b-col>
                <b-col cols="4">
                    <img src="../assets/images/diameter.jpg"/>
                    <img src="../assets/images/diameter_2.jpg"/>
                </b-col>
            </b-row>
            <b-row class="part">
                <b-col cols="2">
                    <div class="number">3</div>
                    Вида материала
                </b-col>
                <b-col class="text">
                    Компания "Аваконт" создает изделия любого оттенка дерева из трех плотных материалов: сосна, ясень, бук, дуб.
                </b-col>
                <b-col cols="4">
                    <b-row>
                        <b-col>
                            <img src="../assets/images/сосна.jpg"  class="materials size"/>
                        </b-col>
                        <b-col>
                            <img src="../assets/images/ясень.jpg"  class="materials size"/>
                        </b-col>
                        <b-col>
                            <img src="../assets/images/бук.jpg"  class="materials size"/>
                        </b-col>
                        <b-col>
                            <img src="../assets/images/дуб.jpg"  class="materials size"/>
                        </b-col>
                    </b-row>
                </b-col>
            </b-row>
            <b-row class="part">
                <b-col cols="2">
                    <div class="number">2</div>
                   Типа стен
                </b-col>
                <b-col class="text">
                    Наши изделия предусмотрены для бревенчатых стен и блок-хауса.
                </b-col>
                <b-col cols="4">
                    <b-row>
                        <b-col>
                            <img src="../assets/images/бревенчатые.jpg" class="size"/>
                        </b-col>
                        <b-col>
                            <img src="../assets/images/блок-хаус.jpg" class="size"/>
                        </b-col>
                    </b-row>
                </b-col>
            </b-row> -->
        </b-container>
    </div>
</template>

<script>
    export default {
        name: "feature",
        data(){
            return{
                calalog:[
                    {
                        number: "30",
                        number_descr:"позиций",
                        number_descr_2:"Более",
                        descr: "Мы изготавливаем более 30 видов деревянных накладок, и продолжаем разрабатывать новые дизайны и функциональность изделий!",
                        img:[
                            {
                                src: "./images/feature/type_1_pad.jpg",
                                alt: "накладка_1_типа",
                            },
                            {
                                src: "./images/feature/type_2_pad.jpg",
                                alt: "накладка_2_типа",
                            },
                        ],
                    },
                    {
                        number:"8",
                        number_descr:" Диаметров бревна",
                        number_descr_2:"",
                        descr: "Мы разработали изделия для 8 самых распространенных размеров бревен. Если у Вас нестандартное бревно, то пишите - мы обязательно что-нибудь придумаем!",
                        img:[
                            {
                                src: "./images/feature/diameters.png",
                                alt: "диаметр_бревна",
                            },
                        ],
                    },
                    {
                        number: "3",
                        number_descr:" Вида материала",
                        number_descr_2:"",
                        descr: " Компания создает изделия любого оттенка дерева из трех плотных материалов: сосна, ясень, бук, дуб.",
                        img:[
                            {
                                src: "./images/feature/pine.jpg",
                                alt: "сосна",
                            },
                            {
                                src: "./images/feature/ash.jpg",
                                alt: "Ясень",
                            },
                            {
                                src: "./images/feature/beech.jpg",
                                alt: "бук",
                            },
                            {
                                src: "./images/feature/oak.jpg",
                                alt: "дуб",
                            },
                        ],
                    },
                    {
                        number: "2",
                        number_descr:"Типа стен",
                        number_descr_2:"",
                        descr: "  Наши изделия предусмотрены для бревенчатых стен и блок-хауса.",
                        img:[
                            {
                                src: "./images/feature/log.jpg",
                                alt: "бревенчатые",
                            },
                            {
                                src: "./images/feature/block-house.jpg",
                                alt: "блок-хаус",
                            },
                        ],
                    },
                ]
            }
        }
    }
</script>
<style scoped lang="scss">

    #feature{
        background: url("../../public/images/background_2.jpg") 100% 100% no-repeat;
        background-size:100% 100%;
        padding-bottom: 5% !important;
    }

    .part{
        border-bottom: 2px solid #7e4614;
    }
    .number{
        font-weight: 400;
        letter-spacing: 4px;
        font-family: 'Lobster', cursive;
        font-size: 4.5rem;
        color: #4f2f0d;
        text-shadow: 1px 1px 1px #ffffff;
    }
    .row:nth-child(3) .number_descr,.row:nth-child(4) .number_descr{
        line-height: 2rem;
    }
    .size{
        box-shadow: 2px 5px 5px #7c5639;
    }
    .row:nth-child(4) .col-4  img{
        border-radius: 50%;
    }
    .row:nth-child(4) .col-4  img,.row:nth-child(5) .col-4 img{
        box-shadow: 2px 5px 5px #7c5639;
    }
    .row:nth-child(5) .col-4 .col {
        padding-left: 5px !important;
        padding-right: 5px !important;
    }

    .col,.col-2,.col-4{
        padding: 1.5% 0.6%;
    }
    .col-2{
        border-bottom: 2px solid #7e4614;
        text-align: center;
        font-weight: 700;
        line-height: 3rem !important;
        font-family: 'Podkova', serif;
        font-size: 1.5rem;
        text-shadow: 1px 1px 1px #7c644c;
        color: #4f2f0d;
    }
    @media screen and (max-width: 500px) {
        .number{
            font-size: 3.5rem !important;
            padding-top: 1.5%;
        }
        .text{
            line-height: 1rem;
            text-shadow: 0.1px 0.1px 0.1px #8f755b;
        }
        .part{
            flex-direction: column;
            .col,.col-2,.col-4{
                max-width: 100% !important;
            }
            .col-2{
                border: none !important;
            }
        }
        .col-4{
                width: 70%;
                display: block;
                margin-left: auto !important;
                margin-right: auto !important;

        }
        img {
            width: 90% !important;
        }
        .col{
            margin-top: -4% !important;
        }
    }
    @media screen and (max-width: 768px) {
        .number{
            font-size: 3rem;
        }
        .col-2 {
            flex: 0 0 20% !important;
            max-width: 20% !important;
        }
        .col-4{
            flex: 0 0 27% !important;
            max-width: 27% !important;
        }
        .col-2{
            font-size: 1rem;
            line-height: 2.5rem !important;
        }
        .col,.col-2{
            padding: 1% 0.6%;
        }
        .text{
            line-height: 1.3rem;
            text-shadow: 0.1px 0.1px 0.1px #8f755b;
        }
    }
    @media screen and (min-width: 768px)and (max-width: 992px) {
        .number{
            font-size: 3.5rem;
        }
        .col-2{
            font-size: 1.2rem;
            line-height: 2.5rem !important;
        }
        .col,.col-2{
            padding: 1% 0.6%;
        }
    }
    @media screen and (min-width: 992px)and (max-width: 1200px) {
        .number{
            font-size: 4rem;
        }
       .col-2{
           font-size: 1.4rem;
           line-height: 2.7rem !important;
       }
        .col,.col-2{
            padding: 1% 0.6%;
        }
    }

</style>