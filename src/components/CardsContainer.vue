
<script>
import{ store } from "../data/store";
import Card from "./partials/Card.vue";

export default {
    name: "CardsContainer",
    components:{
        Card
    },
    data(){
        return{
            store
        }
    }
}
</script>

<template>

  <div class="container p-5">

    <div class="counterCard">
        <p>Found NUMBER Cards</p>
    </div>

    <div class="row">
        <Card/>
        <Card/>
        <Card/>
        <Card/>
        <Card/>
        <Card/>
        <Card/>
        <Card/>
        <Card/>
    </div>
    

  </div>

</template>

<style lang="scss" scoped>

    .container{
        background-color: white;
        min-height: 500px;

        .counterCard{
            background-color: #212529;
            color: white;
            padding: 15px;
            font-weight: bold;
            margin-bottom: 30px;

            p{
                margin: 0;
            }
        }

    }

</style>