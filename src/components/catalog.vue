<template>
    <div id="catalog">
        <b-container>
            <h2>Накладки</h2>
            <h3>Накладки с открытой установкой</h3>
            <div class="flex-container">
                <div v-for="(pad,index) in Open_mount_pads" :key="index">
                    <img :src="pad.src" :alt="pad.alt"/>
                    <h4>{{pad.name_pad}}</h4>
                    <b-button @click="showModal(pad)">
                        <component :is="pad.svg"/>
                    </b-button>
                </div>
            </div>
            <h3>Накладки со скрытой установкой</h3>
            <div class="flex-container">
                <div v-for="(pad,index) in  Flush_mounted_overlays" :key="index">
                    <img :src="pad.src" :alt="pad.alt"/>
                    <h4>{{pad.name_pad}}</h4>
                    <b-button @click="showModal(pad)">
                        <component :is="pad.svg"/>
                    </b-button>
                </div>
            </div>
            <b-modal ref="my-modal"  id="pad" size="lg" centered :title="selectedPad.name">
                <b-row>
                    <b-col cols="4">
                        <img :src="selectedPad.src" :alt="selectedPad.alt"/>
                    </b-col>
                    <b-col>
                        <h3>{{selectedPad.name_pad}}</h3>
                    </b-col>
                </b-row>
                <b-table hover :items="selectedPad.table"></b-table>
            </b-modal>
        </b-container>
    </div>
</template>

<script>
    import DetailsSVG from './more_details_svg';
    import UnderTheRadiator from '../../public/documents/price/under_the_radiator.json';
    export default {
        components: {DetailsSVG},
        name: "catalog",
        data(){
            return{
                selectedPad:{
                    name:"",
                    src:"",
                    alt:"",
                    name_pad:"",
                    svg:'',
                    table:'',
                },
                Open_mount_pads:[
                    {
                        name:"Накладки с открытой установкой",
                        src:"./images/catalog/under_the_radiator.jpg",
                        alt:"Накладка_глухая_под_радиатор",
                        name_pad:"Накладка глухая под радиатор",
                        svg:DetailsSVG,
                        table:UnderTheRadiator,
                    },
                    {
                        name:"Накладки с открытой установкой",
                        src:"./images/catalog/single_on_log.jpg",
                        alt:"Накладка_глухая_одинарная_на_бревно",
                        name_pad:"Накладка глухая одинарная на бревно",
                        svg:DetailsSVG,
                        table:UnderTheRadiator,
                    },
                    {
                        name:"Накладки с открытой установкой",
                        src:"./images/catalog/triple_on_log.jpg",
                        alt:"Накладка_глухая_тройная_на_бревно",
                        name_pad:"Накладка глухая тройная на бревно",
                        svg:DetailsSVG,
                        table:UnderTheRadiator,
                    },
                ],
                Flush_mounted_overlays:[
                    {
                        name:"Накладки со скрытой установкой",
                        src:"./images/catalog/to_the_outlet.jpg",
                        alt:"Накладка_на_розетку",
                        name_pad:"Накладка на розетку",
                        svg:DetailsSVG,
                        table:UnderTheRadiator,
                    },
                    {
                        name:"Накладки со скрытой установкой",
                        src:"./images/catalog/on_switch.jpg",
                        alt:"Накладка_на_выключатель_одинарная",
                        name_pad:"Накладка на выключатель одинарная",
                        svg:DetailsSVG,
                        table:UnderTheRadiator,
                    },
                    {
                        name:"Накладки со скрытой установкой",
                        src:"./images/catalog/double.jpg",
                        alt:"Двойная_накладка",
                        name_pad:"Двойная накладка",
                        svg:DetailsSVG,
                        table:UnderTheRadiator,
                    },
                    {
                        name:"Накладки со скрытой установкой",
                        src:"./images/catalog/double_enlarged.jpg",
                        alt:"Двойная (увеличенная) накладка",
                        name_pad:"Двойная (увеличенная) накладка",
                        svg:DetailsSVG,
                        table:UnderTheRadiator,
                    },
                    {
                        name:"Накладки со скрытой установкой",
                        src:"./images/catalog/triple.jpg",
                        alt:"Тройная накладка",
                        name_pad:"Тройная накладка",
                        svg:DetailsSVG,
                        table:UnderTheRadiator,
                    },
                ],
            }
        },
        methods: {
            showModal(pad) {
                this.selectedPad = pad;
                this.$refs['my-modal'].show()
            }
        }
    }
</script>
<style>
    .modal-footer {
        display: none !important;
    }
    .modal-header{
        background: url("../../public/images/background/background_4.jpg") 100% 100% no-repeat;
        background-size:100% 100%;
        filter: brightness(85%);
        padding: 0.5rem 1rem !important;
        text-decoration: underline;

    }
    .modal-title {
        font-weight: 800 !important;
        font-family: "Tenor Sans", sans-serif;
    }
    .modal-body{
        background: rgba(255, 244, 235, 0.55);
    }
</style>
<style scoped lang="scss">
    #catalog{
        background: url("../../public/images/background/background_2.jpg") 100% 100% no-repeat;
        background-size:100% 100%;
        padding-bottom: 2%;
    }
    .flex-container {
        display: flex;
        flex-wrap: wrap;
    }
    .flex-container > div {
        width: 30%;
        margin: 0 1.5% 2% 1.5% !important;
    }
    .flex-container > div:nth-child(4) {
        margin-left: 18% !important;
    }
    .modal .row{
        padding-bottom: 2% !important;
        .col{
            display: flex;
            align-items: center;
        }
    }
    h2{
        padding-bottom: 0.2% !important;
    }
    h3{
        font-family: 'Viaoda Libre', cursive;
        padding: 0.5% 0;
        font-weight: 800;
        color: #5a330c;
    }
    h3,h4{
        text-align: center;
        text-shadow: 0.5px 0.5px 0.5px #7c644c;
    }
    h4{
        margin-bottom: 0 !important;
        float: left;
        line-height: 1.5rem;
        width: 80%;
        color: black !important;
        height: 3.48rem !important;
        display: flex;
        align-items: center;
        justify-content: center;
        border-top:2px solid #7c644c;
        background: rgba(255, 244, 235, 0.55);
        font-family: 'Viaoda Libre', cursive;
        padding: 2% 0;
        font-weight: 600;
        box-shadow: 2px 5px 5px #977f65;
    }

    .btn{
        font-family: 'Viaoda Libre', cursive;
        float: left;
        font-weight: 800;
        border:2px solid #977f65 ;
        width: 20%;
        height: 3.55rem !important;
        background: rgba(255, 244, 235, 0.55);
        box-shadow: 2px 5px 5px #977f65;
        padding: 0 !important;
    }
    .btn:hover, .btn:focus{
        background: rgb(124, 100, 76,0.45) !important;
        border: none !important;
    }
    img,h4{
        box-shadow: 2px 5px 5px #977f65;
        background: rgba(255, 244, 235, 0.55);
    }
    img{
        filter: contrast(115%) brightness(100%);
    }

    @media screen and (min-width: 768px)and (max-width: 992px) {
        .flex-container > div {
            width: 31%;
            margin: 0 1% 2% 1% !important;
        }
        h4{
            width: 84%;
        }

        .btn{
            width: 16%;
        }
    }
</style>