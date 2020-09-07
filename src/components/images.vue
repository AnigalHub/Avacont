<template>
    <div>
        <b-row>
            <b-col>
                <img src="../assets/images/23.jpg" width="100%"/>
            </b-col>
            <b-col>
                <img src="../assets/images/21.jpg" width="100%"/>
            </b-col>
            <b-col>
                <img src="../assets/images/22.jpg" width="100%"/>
            </b-col>
            <b-col>
                <img src="../assets/images/24.jpg" width="100%"/>
            </b-col>
            <b-col>
                <img src="../assets/images/25.jpg" width="100%"/>
            </b-col>
        </b-row>
    </div>
</template>

<script>
    export default {
        name: "images"
    }
</script>

<style scoped lang="scss">
    .col{
        padding: 0 !important;
    }
    img{
       filter: brightness(55%);
    }
</style>