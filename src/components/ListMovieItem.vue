<script>
import {store} from "../store";
  export default {
     data() {
        return {
          store
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

    <article class="card" style="width: 18rem;">
            <h3 class="card-title">title</h3>
            <h5 class="card-title">original_title</h5>
            <p class="card-text">original_language</p>
            <p class="card-text">vote_average</p>
        
    </article>

</template>

<style scoped>

</style>