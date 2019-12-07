<template>
  <div class="container">
      <h1>Quotes</h1>
      <div class="progress">
  <div class="progress-bar progress-bar-striped" role="progressbar"  aria-valuenow="10" aria-valuemin="0" aria-valuemax="100" :style="{width:(quoteCount/maxNum) * 100 +'%'}">{{quoteCount}}/{{maxNum}}</div>
</div>
  </div>
</template>

<script>
export default {
  props:{
    
    quoteCount:Number,
    maxNum:Number

  },
  

}
</script>

<style scoped>

</style>