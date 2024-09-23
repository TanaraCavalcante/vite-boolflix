<script>
import ListMovieItem from './ListMovieItem.vue';

  export default {
     data() {
        return {
          
        }
  },
  components: {
    ListMovieItem
  }
}
</script>

<template>
  <section class="container">  
    <div class="row">
         <div class="col-6 col-lg-4 my-2" v-for="n in 9">
             <ListMovieItem />
         </div>
    </div>
</section>
</template>

<style scoped>

</style>