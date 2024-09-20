<script>
import SearchBar from './SearchBar.vue';
import MovieList from './MovieList.vue';
import axios from 'axios';

  export default {
     data() {
        return {
          moviesList:[],
          apiUrl:"",
        }
  },
  components:{
    SearchBar,
    MovieList
  },
  methods:{
    getMoviesList(){
      console.log("Chiamata API iniziata!");
      axios.get(this.apiUrl)
        .then((response) => {
           // handle success
           console.log(response);
        })
       .catch(function (error) {
          // handle error
           console.log(error);
        })
        .finally(function () {
          // always executed
          console.log("Chiamata API terminata!")
        });
      }
  },
  created(){
      this.getMoviesList()
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