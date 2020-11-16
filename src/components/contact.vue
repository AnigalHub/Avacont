<template>
    <div id="contact">
        <b-container>
            <h2>Контактная информация</h2>
            <b-row>
                <b-col cols="5">
                    <div class="address text">
                        <div class="telephone">
                            <u> Телефон: </u>
                            <a :href=" link_phone"> {{phone}}</a>
                        </div>
                        <div class="mail">
                            <u>E-mail:</u>
                            <a :href="link_mail">{{mail}}</a>
                        </div>
                        <div>
                            <u>Часы работы: </u><br>
                            {{working_hours}}
                        </div>
                        <div>
                            <u> Адрес производства: </u><br>
                                {{manufacturers_address}}
                        </div>
                        <div>
                            <u> Адрес офиса продаж: </u><br>
                            {{sales_office_address}}
                        </div>
                    </div>
                </b-col>
                <b-col>
                    <div class="feature map" id="map-wrap">
                        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1337.5065661296035!2d37.90404039139417!3d55.68187746704363!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x414ab62f6d977c57%3A0xb6fd3dd42c79d783!2z0YPQuy4g0JjQvdC40YbQuNCw0YLQuNCy0L3QsNGPLCAzNNCQLCDQm9GO0LHQtdGA0YbRiywgTW9zY293IE9ibGFzdCwgMTQwMDAw!5e0!3m2!1sru!2sru!4v1595516566930!5m2!1sru!2sru" frameborder="0"  allowfullscreen="" aria-hidden="false" ></iframe>
                    </div>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import manufacturers_address from '../../public/documents/manufacturers_address';
    import sales_office_address from '../../public/documents/sales_office_address.json';
    export default {
        name: "contact",
        data(){
            return {
                manufacturers_address: manufacturers_address,
                sales_office_address:sales_office_address,
                working_hours:'Пн. – Пт.: с 9:00 до 18:00',
                phone:'+7 (495) 369-26-73',
                link_phone:'tel:+74953692673',
                mail:'avacont@mail.ru',
                link_mail:'mailto:avacont@mail.ru'
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