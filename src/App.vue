<template>
  <div class="container">
    <quote-grid :quotes=quotes></quote-grid>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid';
export default {
  data: function () {
    return {
      maxQuotes: 10,
      quotes: ['Little by little one travels far ']
    }
  },
  components: {
    QuoteGrid
  }
}
</script>

<style>
</style>
