<script>

  export default {
     data() {
        return {  
        }
  },
  props:{
    objectCard:{
        type: Object,
        required: true
    }
  }
}
</script>

<template>

    <article class="card d-flex">
            <h3 class="card-title text-center my-4">{{ objectCard.title }}</h3>
            <p class="card-title text-center">{{ objectCard.original_title }}</p>
            <p class="card-text">{{ objectCard.original_language }}</p>
            <p class="card-text">{{ objectCard.vote_average }}</p>
        
    </article>

</template>

<style lang="scss" scoped>
   article{
      height: 280px;
   }
</style>