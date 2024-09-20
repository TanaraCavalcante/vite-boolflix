<script>
import SearchBar from './SearchBar.vue';
import MovieList from './MovieList.vue';
import axios from 'axios';

  export default {
     data() {
        return {
          moviesList:[]
        }
  },
  components:{
    SearchBar,
    MovieList
  }
}
</script>

<template>
<h1>Main</h1>
   <SearchBar/>
   <MovieList/>
</template>

<style scoped>

</style>