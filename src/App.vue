
<script>
import Header from "./components/Header.vue"
import CardsContainer from "./components/CardsContainer.vue"
import SearchBar from "./components/SearchBar.vue"

export default {
  name: "App",
  components:{
    Header,
    SearchBar,
    CardsContainer
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
