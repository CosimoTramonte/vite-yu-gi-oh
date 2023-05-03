
<script>
import Header from "./components/Header.vue";
import CardsContainer from "./components/CardsContainer.vue";
import SearchBar from "./components/SearchBar.vue";
import Footer from "./components/Footer.vue";
import Loading from "./components/partials/Loading.vue";
import {store} from "./data/store";
import axios from "axios";

export default {
  name: "App",
  components:{
    Header,
    SearchBar,
    CardsContainer,
    Footer,
    Loading
  },
  data(){
    return{
      store
    }
  },
  methods:{
    getApi(){
      store.isLoading = true;
      axios.get(store.apiUrl, {
        params:{
          type: store.type,
          num: store.cardNumber,
          offset: store.cardOffset
        }
      })
      .then(result => {
        store.resultArray = result.data.data;
        store.isLoading = false;
        console.log(store.apiUrl);
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

    <SearchBar @startResearch="getApi" />
    <Loading v-if="store.isLoading" />

    <div v-else>
      <CardsContainer />
      <Footer @startSearch="getApi" />
    </div>

  </div>


</template>


<style lang="scss">

@use "./scss/main.scss";

  .ct-container{
    background-color: #D48F38;
    padding: 8px 50px 80px 50px;
  }

</style>
