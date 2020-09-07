<template>
    <div id="portfolio">
        <b-container>
            <h2>Портфолио</h2>
            <b-row>
                <b-col>
                    <img src="../assets/images/41.jpg"/>
                </b-col>
                <b-col>
                    <img src="../assets/images/42.jpg"/>
                </b-col>
                <b-col>
                    <img src="../assets/images/43.jpg"/>
                </b-col>
                <b-col>
                    <img src="../assets/images/44.jpg"/>
                </b-col>
            </b-row>
            <b-row>
                <b-col>
                    <img src="../assets/images/45.jpg"/>
                </b-col>
                <b-col>
                    <img src="../assets/images/46.jpeg"/>
                </b-col>
                <b-col>
                    <img src="../assets/images/47.jpg"/>
                </b-col>
                <b-col>
                    <img src="../assets/images/48.jpg"/>
                </b-col>
            </b-row>
            <b-row>
                <b-col>
                    <img src="../assets/images/49.jpg"/>
                </b-col>
                <b-col>
                    <img src="../assets/images/50.jpg"/>
                </b-col>
                <b-col>
                    <img src="../assets/images/51.jpg"/>
                </b-col>
                <b-col>
                    <img src="../assets/images/52.jpg"/>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    export default {
        name: "portfolio"
    }
</script>

<style scoped lang="scss">
    #portfolio{
        background: url("../../src/assets/images/background_2.jpg") 100% 100% no-repeat;
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
</style>