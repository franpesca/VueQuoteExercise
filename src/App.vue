<template>
  <div id="app">
    <app-quote-bar :quoteCount="quotes.length" :maxQuotes="maxQuotes" />
    <app-quote-type @quoteAdded="newQuote">
    </app-quote-type>
    <app-quotes :quotes="quotes" @quoteDeleted="deleteQuote" />
    <app-info-bar />
  
  
  </div>
</template>

<script>
  import Quotes from './components/Quotes.vue'
  import QuoteType from './components/QuoteType.vue'
  import InfoBar from './components/InfoBar.vue'
  import QuoteBar from './components/QuoteBar.vue'
  
  export default {
    data() {
      return {
        quotes: ["Asante Sana Cocco Banana"],
        maxQuotes: 10
      }
    },
    methods: {
      // quote come par-arg
      newQuote(quote) {
        if (this.quotes.length > 10) {
          alert('You have reached the max number of quote!')
        } else {
          console.log('debug')
          this.quotes.push(quote)
        }
      },
      deleteQuote(index) {
        this.quotes.splice(index, 1)
      }
    },
    name: 'app',
    components: {
      appQuoteBar: QuoteBar,
      appQuoteType: QuoteType,
      appQuotes: Quotes,
      appInfoBar: InfoBar,
    }
  }
</script>

<style>
  #app {
    margin: auto;
    width: 80%;
    display: flex;
    flex-direction: column;
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  
  
  /* .info-bar {
                  width: 70%;
                  border: 1px solid teal;
                  margin: auto;
                  margin-bottom: 1rem;
              } */
</style>
