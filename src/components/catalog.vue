<template>
    <div id="catalog">
        <b-container>
            <h2>Накладки</h2>
            <h3>Накладки с открытой установкой</h3>
            <div class="flex-container">
                <div v-for="(pad,index) in Open_mount_pads" :key="index">
                    <b-button @click="showModal(pad)">
                        <img :src="pad.src" :alt="pad.alt"/>
                        <h4>{{pad.name_pad}}</h4>
                        <component :is="pad.svg"/>
                    </b-button>
                </div>
            </div>
            <h3>Накладки со скрытой установкой</h3>
            <div class="flex-container">
                <div v-for="(pad,index) in Flush_mounted_overlays" :key="index">
                    <b-button @click="showModal(pad)">
                        <img :src="pad.src" :alt="pad.alt"/>
                        <h4>{{pad.name_pad}}</h4>
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
                <b-table hover :items="selectedPad.table" :fields="fields">
                    <template v-slot:cell(diameter)="{item}">
                        {{item.diameter}} мм
                    </template>
                    <template v-slot:cell(pine)="{item}">
                        {{calcFormula(item.diameter, type.pine)}} руб.
                    </template>
                    <template v-slot:cell(ash)="{item}">
                        {{calcFormula(item.diameter, type.ash)}} руб.
                    </template>
                    <template v-slot:cell(oak)="{item}">
                        {{calcFormula(item.diameter, type.oak)}} руб.
                    </template>
                </b-table>
            </b-modal>
        </b-container>
    </div>
</template>

<script>
    import DetailsSVG from './more_details_svg';
    import Price_table from '../../public/documents/table.json';
    export default {
        components: {DetailsSVG},
        name: "catalog",
        data(){
            return{
                fields: [
                    { label: "Диаметр бревна", key: "diameter" },
                    { label: "Сосна", key: "pine" },
                    { label: "Ясень", key: "ash" },
                    { label: "Бук/Дуб", key: "oak" }
                ],
                selectedPad:{
                    bonus:0,
                    price:0,
                    name:"",
                    src:"",
                    alt:"",
                    name_pad:"",
                    svg:'',
                    table:'',
                },
                type: {
                   pine:0.7,
                   ash: 1.5,
                   oak: 1
                },
                Open_mount_pads:[
                    {
                        bonus:0,
                        price:400,
                        name:"Накладки с открытой установкой",
                        src:"./images/catalog/under_the_radiator.jpg",
                        alt:"Накладка_глухая_под_радиатор",
                        name_pad:"Накладка глухая под радиатор",
                        svg:DetailsSVG,
                        table:Price_table.data,
                    },
                    {
                        bonus:0,
                        price:300,
                        name:"Накладки с открытой установкой",
                        src:"./images/catalog/single_on_log.jpg",
                        alt:"Накладка_глухая_одинарная_на_бревно",
                        name_pad:"Накладка глухая одинарная на бревно",
                        svg:DetailsSVG,
                        table:Price_table.data,
                    },
                    {
                        bonus:0,
                        price:750,
                        name:"Накладки с открытой установкой",
                        src:"./images/catalog/triple_on_log.jpg",
                        alt:"Накладка_глухая_тройная_на_бревно",
                        name_pad:"Накладка глухая тройная на бревно",
                        svg:DetailsSVG,
                        table:Price_table.data,
                    },
                ],
                Flush_mounted_overlays:[
                    {
                        bonus:0,
                        price:350,
                        name:"Накладки со скрытой установкой",
                        src:"./images/catalog/to_the_outlet.jpg",
                        alt:"Накладка_на_розетку",
                        name_pad:"Накладка на розетку",
                        svg:DetailsSVG,
                        table:Price_table.data,
                    },
                    {
                        bonus:0,
                        price:350,
                        name:"Накладки со скрытой установкой",
                        src:"./images/catalog/on_switch.jpg",
                        alt:"Накладка_на_выключатель_одинарная",
                        name_pad:"Накладка на выключатель одинарная",
                        svg:DetailsSVG,
                        table:Price_table.data,
                    },
                    {
                        bonus:0,
                        price:600,
                        name:"Накладки со скрытой установкой",
                        src:"./images/catalog/double.jpg",
                        alt:"Двойная_накладка",
                        name_pad:"Двойная накладка",
                        svg:DetailsSVG,
                        table:Price_table.data,
                    },
                    {
                        bonus:0.1,
                        price:600,
                        name:"Накладки со скрытой установкой",
                        src:"./images/catalog/double_enlarged.jpg",
                        alt:"Двойная (увеличенная) накладка",
                        name_pad:"Двойная (увеличенная) накладка",
                        svg:DetailsSVG,
                        table:Price_table.data,
                    },
                    {
                        bonus:0,
                        price:800,
                        name:"Накладки со скрытой установкой",
                        src:"./images/catalog/triple.jpg",
                        alt:"Тройная накладка",
                        name_pad:"Тройная накладка",
                        svg:DetailsSVG,
                        table:Price_table.data,
                    },
                ],
            }
        },

        methods: {
            showModal(pad) {
                this.selectedPad = pad;
                this.$refs['my-modal'].show()
            },
            calcFormula(diameter, type){
                return (Math.round(((this.selectedPad.price * type * diameter)/ 200)+(((this.selectedPad.price * type * diameter)/ 200) * this.selectedPad.bonus)))
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
    @media screen and (max-width: 500px) {
        .modal-header .close {
            padding: 0.5rem 0.5rem !important;
        }
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
        line-height: 1.5rem;
        width: 80%;
        color: black !important;
        height: 3.48rem !important;
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 2% 1%;
        border-right:1.5px solid #7c644c;
    }
    .btn,h4{
        font-family: 'Viaoda Libre', cursive;
        float: left;
        font-weight: 600;
    }
    .btn{
        background: rgba(255, 244, 235, 0.85);
        box-shadow: 2px 5px 5px #977f65;
        width: 100%;
        padding: 0 !important;
    }
    .btn:hover{
        background: rgba(205, 147, 101, 0.15) !important;
        box-shadow: 2px 5px 5px #504436;
        border: none !important;
    }
    .btn:focus{
        background: rgba(199, 142, 96, 0.25) !important;
    }
    img,.btn{
        box-shadow: 2px 5px 5px #977f65;
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
    }
    @media screen and (min-width: 500px)and (max-width: 768px) {
        .flex-container > div {
            width: 31.5%;
            margin: 0 0.8% 2% 0.8% !important;
        }
        h4{
            width: 80%;
        }
    }
    @media screen and (max-width: 500px) {
        .flex-container > div {
            width: 47%;
            display: block;
            margin-left: auto !important;
            margin-right: auto !important;
            margin-bottom: 5% !important;
        }
        .flex-container > div:nth-child(4) {
            margin-left: auto !important;
        }
        h4{
            width: 80%;
        }
        .col{
            padding-right: 0 !important;
        }
    }
</style>