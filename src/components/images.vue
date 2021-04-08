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
                        src: "./images/images/pad_on_switch.jpg",
                        alt: "Накладка_на_выключатель",
                    },
                    {
                        src: "./images/images/pad_on_2_sockets.jpg",
                        alt: "Накладка_на_2_розетки",
                    },
                    {
                        src: "./images/images/pad_on_night_light.jpg",
                        alt: "Накладка_на_ночник",
                    },
                    {
                        src: "./images/images/triple_pad.jpg",
                        alt: "Тройная_накладка_на_бревно",
                    },
                    {
                        src: "./images/images/pad_between_logs.jpg",
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
        min-height: 65px;
        min-width: 72px;
        width: 100%;
        height: 100%;
    }
</style>