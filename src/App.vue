
<script>
import Header from "./components/Header.vue";
import CardsContainer from "./components/CardsContainer.vue";
import SearchBar from "./components/SearchBar.vue";
import {store} from "./data/store";
import axios from "axios";

export default {
  name: "App",
  components:{
    Header,
    SearchBar,
    CardsContainer
  },
  methods:{
    getApi(){
      axios.get(store.apiUrl)
      .then(result => {
        store.resultArray = result.data;
        console.log(store.resultArray);
      })
    }
  },
  mounted(){
    this.getApi();
  }
}
</script>

<template>

  <Header />
  <div class="ct-container">
    <SearchBar />
    <CardsContainer />
  </div>


</template>


<style lang="scss">

@use "./scss/main.scss";

  .ct-container{
    background-color: #D48F38;
    padding: 8px 50px 80px 50px;
  }

</style>
