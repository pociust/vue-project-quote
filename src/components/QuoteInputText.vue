<template>
  <div class="container frow">
    <div>
      <div class="py-5">Quote</div>
      <input type="text">
      <button @click="addQuote">Add Quote</button>

      </div>
  </div>
</template>

<script>
  export default {
    methods: {
      addQuote() {
        console.log('added')
      }
    }
  
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