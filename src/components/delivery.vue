<template>
    <div id="Delivery">
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

</style>