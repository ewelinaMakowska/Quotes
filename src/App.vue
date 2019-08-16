<template>
  <div class="container">
      <app-progress-bar :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-progress-bar>
      <app-quotes-grid :quotes="quotes" @quoteClicked="deleteQuote"></app-quotes-grid>
      <app-add-quote @quoteEmitted="addNewQuote"></app-add-quote>
  </div>
</template>

<script>
import QuotesGrid from './components/QuotesGrid.vue';
import AddQuote from './components/AddQuote.vue';
import ProgressBar from './components/ProgressBar.vue'

export default {
    data: 
        function() {
            return {
                quotes: [
                    'Example quote',
                    'Second example quote'
                    ],
                maxQuotes: 5
            }
        },
        methods: {
            addNewQuote(quote) {
                if(this.quotes.length >= this.maxQuotes) {
                    alert('Too many quotes! Please delete quote first')
                } else if(quote){
                   this.quotes.push(quote);
                    console.log('Quote added!')
                } else {
                   alert('Please enter quote first')
                }           
            },
            deleteQuote(index) {
                this.quotes.splice(index,1);
            }
        },
        components: {
            appQuotesGrid: QuotesGrid,
            appAddQuote: AddQuote,
            appProgressBar: ProgressBar
        }

    
}

</script>

<style>
</style>
