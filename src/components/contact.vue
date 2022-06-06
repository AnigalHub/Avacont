<template>
    <div id="Contact">
        <div class="background">
        <b-container>
            <h2 class="h2_light">Контактная информация</h2>
            <b-row>
                <b-col cols="5">
                    <div class="address text">
                        <div class="telephone"><u> Телефон:</u><a :href="'tel:'+ address.phone"> {{address.phone}}</a></div>
                        <div class="mail"><u>E-mail:</u><a :href="'mailto:'+ address.mail"> {{address.mail}}</a></div>
                        <div><u>Часы работы:</u><br> {{address.working_hours}}</div>
                        <div><u> Адрес производства:</u><br> {{address.manufacturers_address}}</div>
                        <div><u> Адрес офиса продаж:</u><br> {{address.sales_office_address}}</div>
                    </div>
                </b-col>
                <b-col>
                    <div class="map" id="map-wrap">
                        <iframe title="адрес_компании" :src="address.map" ></iframe>
                    </div>
                </b-col>
            </b-row>
        </b-container>
        </div>
    </div>
</template>

<script>
    import address from '../../public/documents/address.json';
    export default {
        name: "contact",
        data(){
            return {
                address:address,
            }
        }
    }
</script>

<style  scoped lang="scss">

</style>