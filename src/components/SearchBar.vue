<script>


  export default {
     data() {
        return {
          
        }
  },
 
}
</script>

<template>
<div class="d-flex gap-3">
  <input type="text" placeholder="Search a movie" >
  <button class="btn btn-secondary" > Search </button>
</div>

<!--Criado para o main list-->
<ul class="my-3">
  <li>titolo</li>
  <li>titolo originale</li>
  <li>lingua</li>
  <li>voto</li>
</ul>
 

</template>

<style lang="scss" scoped>
  div{
    margin-left: 10px;

    input{
      width: 40%;
    }
  }
</style>