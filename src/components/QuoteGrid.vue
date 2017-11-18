<template>
  <div class="row">
    <quote
      v-for="(quote, index) in quotes"
      :key="index"
      @click.native="deleteQuote(index)" 
      >
      {{ quote }}
      </quote>
  </div>
</template>

<script>
  import Quote from './Quote.vue';

  export default {
    props: ['quotes'],
    components: {
      Quote
    },
    methods: {
      deleteQuote: function (index) {
        this.$emit('quoteDeleted', index);
      }
    }
  }
</script>

<style>

</style>
