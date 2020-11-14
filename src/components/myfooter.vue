<template>
    <div class="myfooter">
        <b-container>
            <b-row>
                <b-col>
                    <a :href=" link_phone"> {{phone}}</a>
                </b-col>
                <b-col>
                    {{address}}
                </b-col>
                <b-col>
                    <a :href="link_mail">{{mail}}</a>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    export default {
        name: "myfooter",
        data(){
            return {
                phone:'+7 (495) 369-26-73',
                link_phone:'tel:+74953692673',
                mail:'avacont@mail.ru',
                link_mail:'mailto:avacont@mail.ru',
                address:'Московская область, г. Люберцы, Инициативная ул., дом 34А, объект 3, офис 5.',
            }
        }
    }
</script>

<style scoped lang="scss">
    .myfooter{
        background: #382b1f;
        background-size:100% 100%;
        padding: 0.8% 0;
    }
    a {
        text-shadow: 0.5px 0.5px 0.5px #7c644c;
        color: rgba(255, 255, 255, 0.9);
    }
    a:hover{
        text-shadow: 0.5px 0.5px 0.5px #7c644c;
        color: rgba(158, 113, 51, 0.53);
        text-decoration: none !important;
        font-weight: 700;
    }
    .col:last-child,.col:first-child{
        padding-top: 2.2%;
    }
    .col{
        cursor: default;
        font-size: 1.15rem;
        text-align: center;
        color: rgba(255, 255, 255, 0.9);
        font-weight: 600;
        font-family: "Tenor Sans", sans-serif;
        text-shadow: 1.2px 1.2px 1.2px #49240c;
    }
    @media screen and (max-width: 500px) {
        .col{
            font-size:0.6rem;
            padding: 0 5px !important;
        }
        .col:last-child,.col:first-child{
            padding-top: 8% !important;
        }
    }
    @media screen and (min-width: 500px)and (max-width: 768px) {
        .col{
            font-size:0.8rem;
        }
        .col:last-child,.col:first-child{
            padding-top: 6%;
        }
    }
    @media screen and (min-width: 768px)and (max-width: 992px) {
        .col{
            font-size: 1rem;
        }
        .col:last-child,.col:first-child{
            padding-top: 4%;
        }
    }
</style>