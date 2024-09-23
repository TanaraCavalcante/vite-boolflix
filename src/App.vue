<script>
import SearchBar from './components/SearchBar.vue';
import AppMain from './components/AppMain.vue';
import axios from 'axios';
  
export default {
     data() {
        return {
          movieListFilter:[],
          selectedItem:'',
          apiUrl: "https://api.themoviedb.org/3/search/movie",
        }
  },
  components:{
    SearchBar,
    AppMain
  },
  methods:{
      logMessage(message){
        console.log(`Chiamo log message con ${message}`);
      },
      getFilterMovies(){
        console.log('chiamata filterMovies iniziata')
        axios.get(this.apiUrl, {
           params: {
              api_key: '97614400969f8d7a2797b6a67b41513b',
              query: avengers,
            }
        })
       
        .then((response) =>{
          console.log(response.data)
        })

        .catch(function (error) {
        console.log(error);
        })

        .finally(function () {
        console.log('Chiamata filter movies terminata!')

        }); 
      }
  }

   
}
</script>

<template>
   <SearchBar />
   <AppMain />
</template>

<style lang="scss">
  @use "./style/general.scss" as *;
  @use "../node_modules/bootstrap/scss/bootstrap.scss" as *;
</style>
