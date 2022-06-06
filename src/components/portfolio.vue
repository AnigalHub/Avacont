<template>
    <div id="Portfolio">
        <b-container>
            <h2>Портфолио</h2>
            <div class="flex-container">
                <img v-for="(work, index) in Portfolio" :key="index" :src="work.src" :alt="work.alt"/>
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
                    {src: "./images/portfolio/round_pad_on_3_sockets.jpg", alt: "Круглая_накладка_на_3_розетки",},
                    {src: "./images/portfolio/round_pad_on_3_switch.jpg", alt: "Квадратная_накладка_на_3_выключателя",},
                    {src: "./images/portfolio/pad_on_log.jpg", alt: "Накладка_на_бревно",},
                    {src: "./images/portfolio/double_pad_on_log.jpg", alt: "Двойная_накладка_на_бревно",},
                    {src: "./images/portfolio/pad_on_switch.jpg", alt: "Накладка_под_выключатель",},
                    {src: "./images/portfolio/pad_with_hidden_installation.jpg", alt: "Накладка_со_скрытой_установкой",},
                    {src: "./images/portfolio/retro_pad.jpg", alt: "Ретро_накладка",},
                    {src: "./images/portfolio/retro_pad_under_log.jpg", alt: "Ретро_накладка_под_бревно",},
                    {src: "./images/portfolio/pad_under_different_sockets.jpg", alt: "Накладка_под_разные_розетки",},
                    {src: "./images/portfolio/pad_under_log_on_switches.jpg", alt: "Накладка_под_бревно_на_выключатели",},
                    {src: "./images/portfolio/pad_of_dark_oak_under_switches.jpg", alt: "Накладка_из_темного_дуба_под_выключатели",},
                    {src: "./images/portfolio/pad_under_socket.jpg", alt: "Накладка_под_розетку",},
                ],
            }
        }
    }
</script>

<style scoped lang="scss">

</style>