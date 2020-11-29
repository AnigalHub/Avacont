<template>
    <div id="delivery">
        <div class="background">
            <b-container>
                <b-row>
                    <b-col><Map></Map></b-col>
                    <b-col>
                        <h2 class="h2_light">Доставка</h2>
                        <div class="text_light">
							<p>Доставка по России курьерской службой СДЭК.</p>
							<p>Особенности доставки зависят от объема заказа и удаленности заказчика.</p>
							<p>Срок доставки от 2х дней.</p>
                        </div>
                    </b-col>
                </b-row>
            </b-container>
        </div>
    </div>
</template>

<script>
    import Map from "./map_svg"
    export default {
        name: "delivery",
        components: {Map},
    }
</script>

<style scoped lang="scss">
    #delivery{
        background: url("../../public/images/background/background_4.jpg") 100% 100% no-repeat;
        background-size:100% 100%;
    }

    @media screen and (max-width: 500px) {
        .text_light{
            line-height: 1.2rem;
        }
    }
    @media screen and (max-width: 768px) {
        .text_light{
            line-height: 1.4rem;
        }
        .col:first-child{
            display: block;
            margin-left: auto;
            margin-right: auto;
            max-width: 65%;
        }
        svg{
            margin-top: -15%;
            padding-bottom: 5%;
        }
        .row{
            flex-direction: column-reverse;
        }
    }

</style>