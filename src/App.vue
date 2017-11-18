<template>
  <div class="container">
    <new-quote @quoteAdded="newQuote"></new-quote>
    <app-header :quoteCount="quotes.length"></app-header>
    <quote-grid
      :quotes="quotes"
      @quoteDeleted="deleteQuote"
    ></quote-grid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert-info">Click on quote to delete!</div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid';
import NewQuote from './components/NewQuote';
import Header from './components/Header';

export default {
  data: function () {
    return {
      maxQuotes: 10,
      quotes: ['Little by little one travels far ']
    }
  },
  components: {
    QuoteGrid,
    NewQuote,
    appHeader: Header
  },
  methods: {
    newQuote: function(quote) {
      this.quotes.push(quote);
    },
    deleteQuote: function(index) {
      this.quotes.splice(index, 1);
    }
  }
}
</script>

<style>
</style>
