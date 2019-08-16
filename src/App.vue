<template>
  <div class="container">
      <app-quotes-grid :quotes="quotes"></app-quotes-grid>
      <app-add-quote @quoteEmitted="addNewQuote"></app-add-quote>
  </div>
</template>

<script>
import QuotesGrid from './components/QuotesGrid.vue';
import AddQuote from './components/AddQuote.vue'

export default {
    data: 
        function() {
            return {
                quotes: [
                    'Example quote',
                    'Second example quote'
                    ],
                maxQuotes: 10
            }
        },
        methods: {
            addNewQuote(quote) {
                this.quotes.push(quote);
                console.log('Quote added!');
            }
        },
        components: {
            appQuotesGrid: QuotesGrid,
            appAddQuote: AddQuote
        }

    
}

</script>

<style>
</style>
