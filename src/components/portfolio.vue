<template>
    <div id="portfolio">
        <b-container>
            <h2>Портфолио</h2>
            <div class="flex-container">
                <div v-for="(work, index) in Portfolio" :key="index">
                    <img :src="work.src" :alt="work.alt"/>
                </div>
            </div>
        </b-container>
    </div>
</template>

<script>
    export default {
        name: "portfolio",
        data(){
            return{
                publicPath: process.env.BASE_URL,
                Portfolio:[
                    {
                        src: "./images/41.jpg",
                        alt: "Круглая_накладка_на_3_розетки",
                    },
                    {
                        src: "./images/42.jpg",
                        alt: "Квадратная_накладка_на_3_выключателя",
                    },
                    {
                        src: "./images/43.jpg",
                        alt: "Накладка_на_бревно",
                    },
                    {
                        src: "./images/44.jpg",
                        alt: "Двойная_накладка_на_бревно",
                    },
                    {
                        src: "./images/45.jpg",
                        alt: "Накладка_под_выключатель",
                    },
                    {
                        src: "./images/46.jpeg",
                        alt: "Накладка_со_скрытой_установкой",
                    },
                    {
                        src: "./images/47.jpg",
                        alt: "Ретро_накладка",
                    },
                    {
                        src: "./images/48.jpg",
                        alt: "Ретро_накладка_под_бревно",
                    },
                    {
                        src: "./images/49.jpg",
                        alt: "Накладка_под_разные_розетки",
                    },
                    {
                        src: "./images/50.jpg",
                        alt: "Накладка_под_бревно_на_выключатели",
                    },
                    {
                        src: "./images/51.jpg",
                        alt: "Накладка_из_темного_дуба_под_выключатели",
                    },
                    {
                        src: "./images/52.jpg",
                        alt: "Накладка_под_розетку",
                    },
                ],
            }
        }
    }
</script>

<style scoped lang="scss">
    .flex-container {
        display: flex;
        flex-wrap: wrap;
    }
    .flex-container > div {
        background: radial-gradient(70% 70%, #ffffff, rgb(210, 206, 211));
        width: 22%;
        margin: 0 1.5% 2.2% 1.5% !important;
    }
    #portfolio{
        background: url("../../public/images/background_2.jpg") 100% 100% no-repeat;
        background-size:100% 100%;
    }
    img{
        box-shadow: 2px 5px 5px #7c5639;
    }
    .row{
        padding-bottom: 15px;
    }
    @media screen and (max-width: 500px) {
        .row{
            padding-bottom: 8px;
        }
        .col{
            padding: 0 4px !important;
        }
    }
    @media screen and (min-width: 500px)and (max-width: 768px) {
        .row{
            padding-bottom: 10px;
        }
        .col{
            padding: 0 10px !important;
        }
    }

    @media screen and  (max-width: 768px) {
        .flex-container > div {
            background: radial-gradient(70% 70%, #ffffff, rgb(210, 206, 211));
            width: 30%;
            margin: 0 1.5% 2.2% 1.5% !important;
        }
    }
</style>