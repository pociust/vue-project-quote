<template>
  <div class="container frow">
    <div>
      <div class="py-5">Quote</div>
      <input type="text" v-model="singleQuote">
      <button @click="addQuote">Add Quote</button>
      <div v-for="quote in quotes" :key="quote.length">
        <Quotes>
          <div>{{ quote }}</div>
        </Quotes>
      </div>

      </div>
  </div>
</template>

<script>
import Quotes from './Quotes.vue';

  export default {
    data() {
      return {
        singleQuote: '',
        quotes: []
      }
    },
    components: {
      Quotes
    },
    methods: {
      addQuote() {
        this.quotes.push(this.singleQuote)

      }
    },
  
  }
</script>

<style scoped>
  .container {
    padding: 50px;
  }
  input {
    height: 75px;
    width: 300px;
    border: 1px solid #333;
    border-radius: 5px;
  }
  button {
    margin: 10px auto;
  }
</style>