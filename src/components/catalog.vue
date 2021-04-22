<template>
    <div id="Catalog">
        <b-container>
            <h2>Накладки</h2>
            <h3>Накладки с открытой установкой</h3>
            <div class="flex-container">
                <div v-for="(pad,index) in price.Open_mount_pads" :key="index">
                    <b-button @click="showModal(pad)">
                        <img :src="pad.src" :alt="pad.alt"/>
                        <h4>{{pad.name_pad}}</h4>
                        <component :is="pad.svg"/>
                    </b-button>
                </div>
            </div>
            <h3>Накладки со скрытой установкой</h3>
            <div class="flex-container">
                <div v-for="(pad,index) in  price.Flush_mounted_overlays" :key="index">
                    <b-button @click="showModal(pad)">
                        <img :src="pad.src" :alt="pad.alt"/>
                        <h4>{{pad.name_pad}}</h4>
                        <component :is="pad.svg"/>
                    </b-button>
                </div>
            </div>
            <b-modal ref="my-modal" id="pad" size="lg" centered :title="selectedPad.name">
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
                        {{calcFormula(item.diameter, price.type.pine)}} руб.
                    </template>
                    <template v-slot:cell(ash)="{item}">
                        {{calcFormula(item.diameter, price.type.ash)}} руб.
                    </template>
                    <template v-slot:cell(oak)="{item}">
                        {{calcFormula(item.diameter, price.type.oak)}} руб.
                    </template>
                </b-table>
            </b-modal>
        </b-container>
    </div>
</template>

<script>
    import DetailsSVG from './more_details_svg';
    import price from '../../public/documents/Pads.json';
    export default {
        components: {DetailsSVG},
        name: "catalog",
        data(){
            return{
                price:price,
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

<style scoped lang="scss">

</style>