<template>
    <div>
        <b-row>
            <b-col v-for="(image, index) in Images" :key="index">
                <img :src="image.src" :alt="image.alt"/>
            </b-col>
        </b-row>
    </div>
</template>

<script>
    export default {
        name: "images",
        data(){
            return{
                Images:[
                    {
                        src: "./images/23.jpg",
                        alt: "Накладка_на_выключатель",
                    },
                    {
                        src: "./images/21.jpg",
                        alt: "Накладка_на_2_розетки",
                    },
                    {
                        src: "./images/22.jpg",
                        alt: "Накладка_на_ночник",
                    },
                    {
                        src: "./images/24.jpg",
                        alt: "Тройная_накладка_на_бревно",
                    },
                    {
                        src: "./images/25.jpg",
                        alt: "Межбревная_наладка",
                    },
                ],
            }
        }
    }
</script>

<style scoped lang="scss">
    .col{
        padding: 0 !important;
    }
    img{
       filter: brightness(55%);
    }
</style>