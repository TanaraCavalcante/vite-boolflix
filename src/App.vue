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
          apiUrl: "https://api.themoviedb.org/3/search/movie?api_key=97614400969f8d7a2797b6a67b41513b&query=",
          store,
          apiUrlSerie:"https://api.themoviedb.org/3/search/tv?api_key=97614400969f8d7a2797b6a67b41513b&language=it_IT&query=friends"
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
      //Chiamata API movies
      getFilterMovies(movieName = ''){
        console.log('chiamata filter MOVIES iniziata');
        axios.get(this.apiUrl, {
          params: {
             query: movieName,
          }
        })
       
        .then((response) =>{
          console.log(response.data.results)
          store.movieListFilter = response.data.results
        })

        .catch(function (error) {
        console.log(error);
        })

        .finally(function () {
        console.log('Chiamata filter MOVIES terminata!')
        });  
      },

      searchMovieInput(inputSearch){
        console.log(`Il parent rispondi: ${inputSearch}`);
        this.getFilterMovies(inputSearch);
      },

      // Chiamata API Series 
      getFilterSeries(){
        console.log('Chiamata filter SERIES iniziata!');
        axios.get(this.apiUrlSerie)
            .then((response) => {
             console.log(response.data.results);
             store.serieListFilter = response.data.results
            })
           .catch(function (error) {
            console.log(error);
           })
           .finally(function () {
            console.log('Chiamata filter SERIES terminata')
           });
      }
  },
  created(){
    this.getFilterMovies();
    this.getFilterSeries();
 }
 
        
}
</script>

<template>
   <p class="my-3">{{ store.message }}</p>
   <AppHeader />
   <SearchBar @search-input="searchMovieInput"/>
   <AppMain />
</template>

<style lang="scss" >

  @use "./style/general.scss" as *;
  @use "../node_modules/bootstrap/scss/bootstrap.scss" as *;
</style>
