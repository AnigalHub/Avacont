<template>
    <div id="catalog">
        <b-container>
            <h2>Накладки</h2>
            <h3>Накладки под розетки  и выключатели на бревно</h3>
            <b-row>
                <b-col>
                    <img src="../assets/images/31.jpg"/>
                    <h4>Накладки с открытой установкой</h4>
                </b-col>
                <b-col>
                    <img src="../assets/images/32.jpg"/>
                    <h4>Накладки со скрытой установкой</h4>
                </b-col>
                <b-col>
                    <img src="../assets/images/33.jpg"/>
                    <h4>Ретро накладки</h4>
                </b-col>
            </b-row>
            <h3>Накладки под розетки и выключатели между бревен</h3>
            <b-row>
                <b-col>
                    <img src="../assets/images/34.jpg"/>
                    <h4>Накладки с открытой установкой</h4>
                </b-col>
                <b-col>
                    <img src="../assets/images/35.jpg"/>
                    <h4>Накладки со скрытой установкой</h4>
                </b-col>
                <b-col>
                    <img src="../assets/images/36.jpg"/>
                    <h4>Ретро накладки</h4>
                </b-col>
            </b-row>
            <b-row>
                <b-col>
                    <h3>Накладки для установки <br> радиаторов и карнизов</h3>
                </b-col>
                <b-col cols="4">
                    <h3>Накладки для установки светильников</h3>
                </b-col>
                <b-row>
                    <b-col>
                        <img src="../assets/images/37.jpg"/>
                        <h4>Накладки на бревно</h4>
                    </b-col>
                    <b-col>
                        <img src="../assets/images/38.jpg"/>
                        <h4>Накладки межбревно</h4>
                    </b-col>
                    <b-col>
                        <img src="../assets/images/39.jpg"/>
                        <h4>Накладки на бревно</h4>
                    </b-col>
                </b-row>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    export default {
        name: "catalog"
    }
</script>

<style scoped lang="scss">
    #catalog{
        background: url("../../src/assets/images/background_2.jpg") 100% 100% no-repeat;
        background-size:100% 100%;
        padding-bottom: 2%;
    }
    h2{
        padding-bottom: 0.2% !important;
    }
    h3{
        font-family: 'Viaoda Libre', cursive;
        padding: 0.5% 0; font-weight: 800;
        color: #5a330c;
    }
    h3,h4{
        text-align: center;
        text-shadow: 0.5px 0.5px 0.5px #7c644c;
    }
    img,h4{
        box-shadow: 2px 5px 5px #977f65;
    }
    h4{
        border-top:2px solid #7c644c;
        background: rgba(255, 244, 235, 0.55);
        font-family: 'Caveat', cursive;
        padding: 2% 0;
        height: auto;
        font-weight: 600;
        color:  #4E2B0B;
    }
    .col{
        padding-left: 25px !important;
        padding-right: 25px !important;
    }
    .col-4{
        padding-left: 5px !important;
        padding-right: 5px !important;
    }
    @media screen and (max-width: 768px) {
        .col{
            padding-left: 5px !important;
            padding-right: 5px !important;
        }
    }
</style>