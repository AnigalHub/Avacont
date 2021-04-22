<template>
    <div id="Home">
        <div id="background">
            <b-container>
                <h1>Накладки на бревно и блок-хаус</h1>
                <b-row>
                    <b-col>
                        <div class="text_light">Изготовление накладок из дерева под розетки, выключатели, радиаторы, светильники и карнизы разных производителей.</div>
                        <ul>
                            <li v-for="(feature,index) in Features" :key="index">{{feature}}</li>
                        </ul>
                    </b-col>
                    <b-col>
                        <b-carousel
                                id="carousel-fade" fade indicators>
                            <b-carousel-slide>
                                <template v-slot:img>
                                    <img src="../../public/images/home/double_pad.jpg" alt="двойная_накладка"/>
                                </template>
                            </b-carousel-slide>
                            <b-carousel-slide>
                                <template v-slot:img>
                                    <img src="../../public/images/home/log_pad.jpg" alt="накладка_на_выключатель"/>
                                </template>
                            </b-carousel-slide>
                            <b-carousel-slide>
                                <template v-slot:img>
                                    <img src="../../public/images/home/pad_on_switch.jpg" alt="накладка_на_розетку"/>
                                </template>
                            </b-carousel-slide>
                            <b-carousel-slide>
                                <template v-slot:img>
                                    <img src="../../public/images/home/triple_pad.jpg" alt="тройная_накладка"/>
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

<style scoped lang="scss">

</style>