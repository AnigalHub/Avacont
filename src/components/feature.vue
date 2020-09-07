<template>
    <div id="feature">
        <b-container>
            <h2>Характеристики изделий</h2>
            <b-row class="part">
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
                    Компания "Аваконт" создает изделия любого оттенка дерева из трех плотных материалов: ясень, бук, дуб.
                </b-col>
                <b-col cols="4">
                    <b-row>
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
            </b-row>
        </b-container>
    </div>
</template>

<script>
    export default {
        name: "feature"
    }
</script>

<style scoped lang="scss">
    #feature{
        background: url("../../src/assets/images/background_2.jpg") 100% 100% no-repeat;
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
    .size{
        box-shadow: 2px 5px 5px #7c5639;
    }
    .materials{
        border-radius: 50%;
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