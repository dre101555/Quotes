<template>
  <div id="app">
      <Header :quoteCount="quotes.length" :maxNum="max"/>
      <br>
      <QuoteCreate @send="newQuote"/>
      <br>
      <QuoteGrid :quotes="quotes"  @delete="deleteQuote" />
      <br>
      <div class="col-sm-12 text-center">
        <div class="alert alert-primary" role="alert">
               Click on Quote to delete it 
        </div>
      </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import QuoteCreate from './components/QuoteCreate.vue'
import QuoteGrid from './components/QuoteGrid.vue'


export default {

  data(){
    return{
          quotes:['Work smart ,not Hard'],
          max:10
    }
  },
  methods:{

    newQuote(userInput){
        if(this.quotes.length >= this.max){
            alert("List is full.Please delete 1 Item!!!!")
        }else{
            this.quotes.push(userInput)
        }
          

    },
    deleteQuote(index){
      this.quotes.splice(index,1)
    }

  },

  components: {
    Header,
    QuoteCreate,
    QuoteGrid
   
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
