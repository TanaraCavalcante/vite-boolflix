<script>
import AppMain from './components/AppMain.vue';
import SearchBar from './components/SearchBar.vue';
import AppHeader from './components/AppHeader.vue';
import axios from 'axios';
import {store} from "./store" 
  
export default {
     data() {
        return {
          selectedItem:'',
          apiUrl: "https://api.themoviedb.org/3/search/movie?api_key=97614400969f8d7a2797b6a67b41513b&query=avengers",
          store
        }
  },
  components:{
    AppMain,
    SearchBar,
    AppHeader
  },
  methods:{
      logMessage(message){
        console.log(`Chiamo log message con ${message}`);
      },
      //Chiamata API
      getFilterMovies(){
        console.log('chiamata filterMovies iniziata')
        axios.get(this.apiUrl, {
           //deveriam ter os parametros
        })
       
        .then((response) =>{
          console.log(response.data.results)
          store.movieListFilter = response.data.results
        })

        .catch(function (error) {
        console.log(error);
        })

        .finally(function () {
        console.log('Chiamata filter movies terminata!')

        });  
      }
  },
  created(){
  this.getFilterMovies();
 }
 
        
}
</script>

<template>
   <h1>{{ store.message }}</h1>
   <AppHeader />
   <SearchBar />
   <AppMain />
</template>

<style lang="scss">
  @use "./style/general.scss" as *;
  @use "../node_modules/bootstrap/scss/bootstrap.scss" as *;
</style>
