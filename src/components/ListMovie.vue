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
    <div class="row">
         <div class="col-6 col-lg-4 my-2" v-for="(movieListFilterItem, i) in store.movieListFilter" :key="i" :objectCard="movieListFilterItem" >
             <ListMovieItem :objectCard="movieListFilterItem"/>
         </div>
    </div>
    <span>A lista tem {{ store.movieListFilter.length }} filmes!</span>
</section>
</template>

<style scoped>

</style>