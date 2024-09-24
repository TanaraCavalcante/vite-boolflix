<script>
import ListSerieItem from "./ListSerieItem.vue";
import {store} from "../store"

  export default {
     data() {
        return {
          store
        }
  },
  components: {
    ListSerieItem
  }
}
</script>

<template>
<section class="container">  
    <div class="row">
         <div class="col-6 col-lg-3 my-2" v-for="(serieListFilterItem, i) in store.serieListFilter" :key="i" :serieCard="serieListFilterItem" >
             <ListSerieItem />
         </div>
    </div>
    <span>A lista tem {{ store.serieListFilter.length }} Tv Series!</span>

</template>

<style scoped>

</style>