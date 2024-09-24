<script>

  export default {
     data() {
        return {
          searchMovie:'',
        }
  },
  methods:{
    getSearchedMovie(searchMovie){
      console.log(`Cerca questo filme: ${this.searchMovie}`)
      
    }
  }
 
}
</script>

<template>
<div class="d-flex gap-3 my-3">
  <input type="text" placeholder="Search a movie" v-model="searchMovie">
  <button class="btn btn-secondary" @click="getSearchedMovie"> Search </button>
</div>

</template>

<style lang="scss" scoped>
  div{
    margin-left: 10px;

    input{
      width: 40%;
    }
  }
</style>