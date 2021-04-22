<template>
    <div id="Feature">
        <b-container>
            <h2>Характеристики изделий</h2>
            <b-row class="part" v-for="(catalog, index) in catalog" :key="index">
                <b-col cols="2">
                    <div class="number_descr">{{catalog.number_descr_2}}</div>
                    <div class="number">{{catalog.number}}</div>
                    <div class="number_descr">{{catalog.number_descr}}</div>
                </b-col>
                <b-col class="text">{{catalog.descr}}</b-col>
                <b-col cols="4">
                    <b-row>
                        <b-col  v-for="(value, index) in catalog.img" :key="index">
                            <img :src="value.src" :alt="value.alt"/>
                        </b-col>
                    </b-row>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    export default {
        name: "feature",
        data(){
            return{
                catalog:[
                    {
                        number: "30",
                        number_descr:"позиций", number_descr_2:"Более",
                        descr: "Мы изготавливаем более 30 видов деревянных накладок, и продолжаем разрабатывать новые дизайны и функциональность изделий!",
                        img:[
                            {src: "./images/feature/type_1_pad.jpg", alt: "накладка_1_типа",},
                            {src: "./images/feature/type_2_pad.jpg", alt: "накладка_2_типа",},
                        ],
                    },
                    {
                        number:"8",
                        number_descr:" Диаметров бревна", number_descr_2:"",
                        descr: "Мы разработали изделия для 8 самых распространенных размеров бревен. Если у Вас нестандартное бревно, то пишите - мы обязательно что-нибудь придумаем!",
                        img:[
                            {src: "./images/feature/diameters.png", alt: "диаметр_бревна",},
                        ],
                    },
                    {
                        number: "3",
                        number_descr:" Вида материала", number_descr_2:"",
                        descr: " Компания создает изделия любого оттенка дерева из трех плотных материалов: сосна, ясень, бук, дуб.",
                        img:[
                            {src: "./images/feature/pine.jpg", alt: "сосна",},
                            {src: "./images/feature/ash.jpg", alt: "Ясень",},
                            {src: "./images/feature/beech.jpg", alt: "бук",},
                            {src: "./images/feature/oak.jpg", alt: "дуб",},
                        ],
                    },
                    {
                        number: "2",
                        number_descr:"Типа стен", number_descr_2:"",
                        descr: "Наши изделия предусмотрены для бревенчатых стен и блок-хауса.",
                        img:[
                            {src: "./images/feature/log.jpg", alt: "бревенчатые",},
                            {src: "./images/feature/block-house.jpg", alt: "блок-хаус",},
                        ],
                    },
                ]
            }
        }
    }
</script>

<style scoped lang="scss">

</style>