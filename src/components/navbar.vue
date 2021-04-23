<template>
    <b-navbar id="Nav" class="navbar-expand-xl sticky-top" toggleable>
        <b-container>
            <b-navbar-brand href="#Home" @click.prevent="scrollToTop()">
                <img src="../../public/favicon.jpg" alt="логотип_компании"/>
                <div class="name_company">АВАКОНТ</div>
                <div class="description_name">производственная компания</div>
            </b-navbar-brand>
            <b-navbar-toggle target="navbar-toggle-collapse">
                <template v-slot:default="{ expanded }">
                    <b-icon v-if="expanded" icon="chevron-bar-up"></b-icon>
                    <b-icon v-else icon="chevron-bar-down"></b-icon>
                </template>
            </b-navbar-toggle>
            <b-collapse id="navbar-toggle-collapse" class="justify-content-end" is-nav v-model="isExpanded">
                <b-navbar-nav>
                    <b-nav-item @click="scrollToId" href="#Features">Характеристики</b-nav-item>
                    <b-nav-item @click="scrollToId" href="#Catalog">Каталог</b-nav-item>
                    <b-nav-item @click="scrollToId" href="#Delivery">Доставка</b-nav-item>
                    <b-nav-item @click="scrollToId" href="#Portfolio">Наши работы</b-nav-item>
                    <b-nav-item @click="scrollToId" href="#Contact">Контакты</b-nav-item>
                </b-navbar-nav>
            </b-collapse>
        </b-container>
    </b-navbar>
</template>


<script>
    export default {
        name: "navbar",
        data(){
            return {
                isExpanded: false,
            }
        },
        methods:{
            scrollToTop(){
                window.scrollTo({top: 0, left: 0, behavior: 'smooth' });
            },
            scrollToId(event){
                let offsetY = 0;
                if(this.isExpanded){
                    let nav = document.getElementById(("Nav"));
                    let bounds =  nav.getBoundingClientRect();
                    offsetY = bounds.height;
                }
                let element = document.getElementById(event.target.hash.replace("#", ""));
                window.scrollTo({top: element.offsetTop - offsetY, left: 0, behavior: 'smooth'});
                event.preventDefault();
            }
        }
    }
</script>

<style scoped lang="scss">
    /*блок под логотип(картинка, название компании, что за компания(производственная))*/
    .navbar-brand{
        padding-top: 0.2rem !important;
        padding-bottom: 0.2rem !important;
    }
    /*картинка в логотипе*/
    img{
        height: 40px !important;
        width: 40px !important;
        float: left !important;
        border: 1px solid rgba(78, 43, 11, 0.75);
        box-shadow: 0.1em 0.1em 0.2em #8f745c;
        margin-right: 4px;
        border-radius: 7px;
    }
    /*меню на всех экранах (которое будет и складываться на маленьких экранах и раскрываться на больших)*/
    .navbar{
        background: #b8a59c;
        background-size:cover;
        border-bottom: 5px #4E2B0B !important;
        padding: 0 !important;
    }
    /*все кнопки в меню*/
    .nav-link{
        color: #4E2B0B !important;
        padding-right: 1rem !important;
        padding-left: 1rem !important;
        font-weight: 600;
        font-size: 1.3rem !important;
        &:hover{ /*при наведении*/
            font-weight: 700;
            text-decoration: underline;
            text-shadow: 0.2em 0.2em 0.3em #8f745c;
        }
    }
    /*название компании "Аваконт" в логотипе*/
    .name_company{
        font-size: 1.4rem;
        color: #4E2B0B;
        font-weight: 700;
        font-style: italic;
        letter-spacing: 9px;
        font-family: "Caveat", cursive;
    }
    /*надпись "производственная компания" в логотипе*/
    .description_name{
        font-size: 0.65rem;
        margin-top: -6%;
        color: #4E2B0B;
        font-weight: 600;
        text-shadow: 0.025rem 0.025rem 0.025rem #4e2b0b;
    }
    @media screen and (max-width: 768px) {
        /*все кнопки в меню*/
        .nav-link {
            font-size: 1rem !important;
            padding: 0.35rem 1rem !important;
        }
    }
</style>