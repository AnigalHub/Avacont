<template>
    <b-navbar class="navbar-expand-xl sticky-top " toggleable>
        <b-container>
            <b-navbar-brand>
                <img src="../assets/images/hands.jpg"  style="float: left" width="40px" height="40px"/>
                <div class="name_company"> АВАКОНТ</div>
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
                    <b-nav-item>Характеристики</b-nav-item>
                    <b-nav-item>Каталог</b-nav-item>
                    <b-nav-item>Доставка</b-nav-item>
                    <b-nav-item>Наши работы</b-nav-item>
                    <b-nav-item>Контакты</b-nav-item>
                </b-navbar-nav>
            </b-collapse>
        </b-container>
    </b-navbar>
</template>

<script>
    export default {
        name: "navbar"
    }
</script>

<style scoped lang="scss">
    img{
        height: 40px !important;
        width: 40px !important;
    }
    .navbar{
        background: url("../assets/images/navbar.jpg") 100% 100% no-repeat;
        background-size:cover;
        padding: 0 !important;
    }
    .nav-link{
        color: #4E2B0B !important;
        padding-right: 1rem !important;
        padding-left: 1rem !important;
        font-weight: 600;
        font-size: 1.15rem !important;
        font-family: 'Tenor Sans', sans-serif;
    }
    .nav-link:hover{
        font-weight: 700;
        text-decoration: underline;
        text-shadow: 0.2em 0.2em 0.3em #8f745c;
    }
    .name_company{
        font-size: 1.6rem;
        color: #4E2B0B;
        font-weight: 700;
        letter-spacing: 7px;
        font-family: 'Caveat', cursive;
    }
    .description_name{
        font-size: 0.63rem;
        margin-top: -6%;
        color: #4E2B0B;
        text-shadow: 0.05em 0.05em 0.05em #4E2B0B;
        font-weight: 500;
    }
    img{
        border: 1px solid rgba(78, 43, 11, 0.75);
        box-shadow: 0.1em 0.1em 0.2em #8f745c;
        margin-right: 4px;
        border-radius: 7px;
    }
</style>