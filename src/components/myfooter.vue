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
        /*ссылки*/
        a {
            text-shadow: 0.5px 0.5px 0.5px #7c644c;
            color: rgba(255, 255, 255, 0.9);
            /*при наведении*/
            &:hover{
                text-shadow: 0.5px 0.5px 0.5px #7c644c;
                color: rgba(158, 113, 51, 0.53);
                text-decoration: none !important;
                font-weight: 700;
            }
        }
        /*параметры сетки бутстрап (блок под информацию)*/
        .col{
            cursor: default;
            font-size: 1.25rem;
            text-align: center;
            color: rgba(255, 255, 255, 0.9);
            font-weight: 600;
            text-shadow: 1.2px 1.2px 1.2px #49240c;
            /*блок с телефоном и блок с почтой*/
            &:last-child,&:first-child{padding-top: 2.2%;}
        }
    }

    @media screen and (max-width: 500px) {
        #Myfooter {
            /*параметры сетки бутстрап (блок под информацию)*/
            .col {
                font-size: 0.8rem;
                letter-spacing: -.8px;
                padding: 0 5px !important;
                /*блок с телефоном и блок с почтой*/
                &:last-child, &:first-child {padding-top: 8% !important;}
            }
        }
    }
    @media screen and (min-width: 500px)and (max-width: 768px) {
        #Myfooter {
            /*параметры сетки бутстрап (блок под информацию)*/
            .col {
                font-size: 1rem;
                /*блок с телефоном и блок с почтой*/
                &:last-child, &:first-child {padding-top: 6%;}
            }
        }
    }
    @media screen and (min-width: 768px)and (max-width: 992px) {
        #Myfooter {
            /*параметры сетки бутстрап (блок под информацию)*/
            .col {
                font-size: 1rem;
                /*блок с телефоном и блок с почтой*/
                &:last-child, &:first-child {padding-top: 4%;}
            }
        }
    }
</style>