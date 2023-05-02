
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
  data(){
    return{
      store
    }
  },
  methods:{
    getApi(){
      axios.get(store.apiUrl + '?num=100&offset=0')
      .then(result => {
        store.resultArray = result.data.data;
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
