<script>
import SearchBar from './SearchBar.vue';
import MovieList from './MovieList.vue';

  export default {
     data() {
        return {
          
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