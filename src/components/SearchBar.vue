
<script>
import {store} from "../data/store";
import typeMenu from "../data/db";

export default {
    name: "SearchBar",
    data(){
        return{
            store,
            typeMenu
        }
    }
}
</script>

<template>

<div class="container d-flex p-4">
    <select v-model="store.type"  class="form-select">
        <option v-for="(option,index) in typeMenu" :key="index" :value="option">{{ option }}</option>
    </select>
    <button class="btn btn-dark mx-3" @click="$emit('startResearch')">Search</button>
</div>


</template>

<style lang="scss" scoped>

    select{
        width: 20%;
    }

</style>