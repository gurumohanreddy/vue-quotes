<template>
  <div class="container">
    <div>
      <h1 class="text-center">Vue Quotes</h1>
      <quote-header :quotesCount="quotes.length" :maxQuotes="maxQuotes"></quote-header>
      <quote-input @addedQuote="newQuote"></quote-input>
      <quote-grid :quotes="quotes" @deleteQuote="deleteQuote"></quote-grid>
      <div class="alert alert-info" role="alert">
        Tip: Click on the quote to delete it.
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import QuoteInput from './components/QuoteInput.vue';
import QuoteHeader from './components/header.vue';
export default {
  data: function(){
    return {
      quotes: ['Dummy Quote to get started'],
      maxQuotes: 10
    }
  },
  components: {
    QuoteGrid,
    QuoteInput,
    QuoteHeader
  },
  methods: {
    newQuote(quote) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert('Please delete Quotes First!');
      }
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  }
}
</script>

<style>
</style>
