<template>
  <div class="row"> 
      <Quote v-for="(x,index) in quotes" :key="index" @click.native="deleteQuote(index)">
          <template>{{x}}</template>
      </Quote>
  </div>
</template>

<script>

import Quote from './Quote.vue'
export default {
   
    props:{
                quotes:String
            },
    components:{
        Quote
    },
    methods:{
      deleteQuote(index){
          this.$emit('delete',index)
      }
    }

}
</script>

<style>

</style>