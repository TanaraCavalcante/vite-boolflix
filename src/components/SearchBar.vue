<script>

  export default {
     data() {
        return {
          searchContent:'',
        }
  },
  methods:{
    getSearchedContent(message){
      console.log(`il figlio cerca questo contenuto: ${message}`);
      this.$emit("searchInput", message )
    }
  }
 
}
</script>

<template>
<div class="d-flex gap-3 my-3">
  <input type="text" placeholder=" What do you want to wach?" v-model="searchContent">
  <button class="btn btn-secondary" @click="getSearchedContent(searchContent)"> Search </button>
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