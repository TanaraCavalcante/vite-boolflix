<script>

  export default {
     data() {
        return {
          
        }
  },
  props:{
    serieCard:{
        type: Object,
        required: true
    }
  }
}
</script>

<template>

    <article class="card d-flex">
            <h3 class="card-title text-center my-4">{{ serieCard.name}}</h3>
            <p class="card-title text-center">{{ serieCard.original_name }}</p>
            <p class="card-text">{{serieCard.original_language}}</p>
            <p class="card-text">{{serieCard.vote_average }}</p>
        
    </article>

</template>

<style lang="scss" scoped>
   article{
      height: 280px;
      h3{
        color: darkblue;
      }
   }
</style>