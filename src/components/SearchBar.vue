<script>
  export default {
     data() {
        return {
          movieListFilter:[],
          selectedItem:'',
        }
  },
  methods:{
      logMessage(message){
        console.log(`Chiamo log message con ${message}`);
      }
  }
}
</script>

<template>
<div class="d-flex gap-3">
  <input type="text" placeholder="Search a movie" >
  <button class="btn btn-secondary" > Search </button>
 
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