<template>
  <div class="container frow">
    <div v-if="quoteLengthLimitation < 10">
      <div class="py-5">Quote</div>
      <input type="text" v-model="singleQuote">
      <button @click="addQuote" type="button">Add Quote</button>
    </div>
    <div v-if="quoteLengthLimitation >= 10" class="danger-alert">
      Please delete a quote before adding a new one!
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
    props: {
      quoteLengthLimitation: {
        type: Number
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

  .danger-alert {
    background-color: red;
    padding: 50px;
    color: white;
    font-size: 25px;
  }
</style>