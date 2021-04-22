<template>
    <div id="Myfooter">
        <b-container>
            <b-row>
                <b-col><a :href="'tel:'+ address.phone"> {{address.phone}}</a></b-col>
                <b-col>{{address.manufacturers_address}}</b-col>
                <b-col><a :href="'mailto:'+ address.mail">{{address.mail}}</a></b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import address from '../../public/documents/address.json';
    export default {
        name: "myfooter",
        data(){
            return {
                address:address,
            }
        }
    }
</script>

<style scoped lang="scss">
    #Myfooter{
        background: #382b1f;
        background-size:100% 100%;
        padding: 0.8% 0;
        a { /*ссылки*/
            text-shadow: 0.5px 0.5px 0.5px #7c644c;
            color: rgba(255, 255, 255, 0.9);
            &:hover{
                text-shadow: 0.5px 0.5px 0.5px #7c644c;
                color: rgba(158, 113, 51, 0.53);
                text-decoration: none !important;
                font-weight: 700;
            }
        }
        .col{ /*параметры сетки бутстрап (блок под информацию)*/
            cursor: default;
            font-size: 1.25rem;
            text-align: center;
            color: rgba(255, 255, 255, 0.9);
            font-weight: 600;
            text-shadow: 1.2px 1.2px 1.2px #49240c;
            &:last-child,&:first-child{padding-top: 2.2%;}/*блок с телефоном и блок с почтой*/
        }
    }

    @media screen and (max-width: 500px) {
        #Myfooter {
            .col {  /*параметры сетки бутстрап (блок под информацию)*/
                font-size: 0.8rem;
                letter-spacing: -.8px;
                padding: 0 5px !important;
                &:last-child, &:first-child {padding-top: 8% !important;}/*блок с телефоном и блок с почтой*/
            }
        }
    }
    @media screen and (min-width: 500px)and (max-width: 768px) {
        #Myfooter {
            .col {  /*параметры сетки бутстрап (блок под информацию)*/
                font-size: 1rem;
                &:last-child, &:first-child {padding-top: 6%;}/*блок с телефоном и блок с почтой*/
            }
        }
    }
    @media screen and (min-width: 768px)and (max-width: 992px) {
        #Myfooter {
            .col {  /*параметры сетки бутстрап (блок под информацию)*/
                font-size: 1rem;
                &:last-child, &:first-child {padding-top: 4%;} /*блок с телефоном и блок с почтой*/
            }
        }
    }
</style>