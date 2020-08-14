<template>
  <div class="container frow">
    <div>
      <div class="py-5">Quote</div>
      <input type="text" v-model="singleQuote">
      <button @click="addQuote">Add Quote</button>
    </div>
  </div>
</template>

<script>
import Quotes from './Quotes.vue';

  export default {
    data() {
      return {
        singleQuote: '',
      }
    },
    components: {
      Quotes
    },
    methods: {
      addQuote() {
        this.$emit('singleQuoteToPush', this.singleQuote)

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