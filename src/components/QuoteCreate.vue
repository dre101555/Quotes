<template>
  <div class="container"> 
    <form>
        <div class="form-group">
            <textarea name="" id="" cols="30" rows="10" v-model="userInput"></textarea>
        </div>
        <button type="button" class="btn btn-primary" @click.prevent="sendData">Submit</button>
    </form>
  </div>
</template>

<script>
export default {
  data(){
    return{
      userInput:""
    }
  },
  methods:{
    sendData(){
      this.$emit('send',this.userInput)
    }
  }

}
</script>

<style>

</style>