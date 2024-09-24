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
            <h3 class="card-title text-center my-4">{{ }}titolo</h3>
            <p class="card-title text-center">{{  }}titolo-original</p>
            <p class="card-text">{{ }}linguagem</p>
            <p class="card-text">{{ }}voto</p>
        
    </article>

</template>

<style lang="scss" scoped>
   article{
      height: 260px;
   }
</style>