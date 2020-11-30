<template>
    <div id="contact">
        <b-container>
            <h2>Контактная информация</h2>
            <b-row>
                <b-col cols="5">
                    <div class="address text">
                        <div class="telephone">
                            <u> Телефон: </u><a :href="'tel:'+ address.phone"> {{address.phone}}</a>
                        </div>
                        <div class="mail">
                            <u>E-mail:</u><a :href="'mailto:'+ address.mail">{{address.mail}}</a>
                        </div>
                        <div>
                            <u>Часы работы: </u><br>{{address.working_hours}}
                        </div>
                        <div>
                            <u> Адрес производства: </u><br>{{address.manufacturers_address}}
                        </div>
                        <div>
                            <u> Адрес офиса продаж: </u><br>{{address.sales_office_address}}
                        </div>
                    </div>
                </b-col>
                <b-col>
                    <div class="feature map" id="map-wrap">
                        <iframe :src="address.map" ></iframe>
                    </div>
                </b-col>
            </b-row>
        </b-container>
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
    #contact{
    background: url("../../public/images/background/background_2.jpg") 100% 100% no-repeat;
    background-size:100% 100%;
    padding-bottom: 2.5%;
    }
    a {
        text-shadow: 0.5px 0.5px 0.5px #7c644c;
        color: #6a4827;
    }
    a:hover{
        text-shadow: 0.5px 0.5px 0.5px #7c644c;
        color: #5a3827;
        text-decoration: none !important;
        font-weight: 700;
    }
    .col-5 div{
        padding-bottom: 2%;
    }
    u{
        font-size: 1.5rem;
        text-shadow: 0.5px 0.5px 0.5px #7c644c;
        color: #40200b;
        font-weight: 600;
    }
    .address{
        padding: 4%;
        background: linear-gradient(to right top,rgba(131, 108, 84, 0.35),rgba(131, 108, 84, 0.15),rgba(131, 108, 84, 0.35));
        border-radius: 8px;
        box-shadow: 2px 5px 5px #7c5639;
    }

    .feature.map {
        padding-top: 1%;
        iframe {
            min-height: 460px;
            height: auto;
            width:100% !important;
            border:0;
            filter: brightness(95%);
        }
    }
    @media screen and (max-width: 500px) {
        u {
            font-size: 0.9rem;
        }
        .col-5, .col {
            padding: 0 5px !important;
        }
        .mail, .telephone {
            display: none;
        }
        .row {
            flex-direction: column;
            .col-5 {
                max-width: 100% !important;
                margin-bottom: 2%;
            }
        }
        .col-5 div {
            padding-bottom: 0.2%;
        }
        .text {
            line-height: 1.2rem;
        }
        .feature.map {
            padding-top: 1%;
            iframe {
                min-height: 300px;
            }
        }
        .address {
            padding: 1%;
        }
    }
    @media screen and (min-width: 500px)and (max-width: 768px) {
        u {
            font-size: 1.2rem;
        }
        .col-5, .col {
            padding: 0 5px !important;
        }
        .mail, .telephone {
            display: none;
        }
        .row {
           flex-direction: column;
            .col-5 {
                max-width: 100% !important;
                margin-bottom: 2%;
            }
        }
        .col-5 div {
            padding-bottom: 0.2%;
        }
        .text {
            line-height: 1.4rem;
        }
        .feature.map {
            padding-top: 1%;
            iframe {
                min-height: 300px;
            }
        }
        .address {
            padding: 1%;
        }
    }
    @media screen and (min-width: 768px)and (max-width: 992px) {
        u{
            font-size: 1.2rem;
        }
    }
    @media screen and (min-width: 992px)and (max-width: 1200px) {
        u{
            font-size: 1.4rem;
        }
    }
</style>