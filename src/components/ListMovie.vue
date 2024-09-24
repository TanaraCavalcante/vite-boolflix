<script>
import ListMovieItem from './ListMovieItem.vue';
import {store} from "../store"

  export default {
     data() {
        return {
          store
        }
  },
  components: {
    ListMovieItem
  }
}
</script>

<template>
  <section class="container"> 
    <span class="fw-bolder my-4 h3">A lista tem {{ store.movieListFilter.length }} filmes!</span> 
    <div class="row">
         <div class="col-6 col-lg-3 my-2" v-for="(movieListFilterItem, i) in store.movieListFilter" :key="i" :objectCard="movieListFilterItem" >
             <ListMovieItem :objectCard="movieListFilterItem"/>
         </div>
    </div>  
</section>
</template>

<style lang="scss" scoped>
  //  span {
  //   text-align: center;
  //   font-weight: bolder;
  //  }

</style>