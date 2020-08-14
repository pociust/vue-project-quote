<template>
  <div>
    <div class="header">
      Quotes Added
    </div>
    <div class="outter-box">
      <div class="inner-box" :style="{width: (numQuotes * 10 ) + '%'}">
        {{ numQuotes }}/10
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        numQuotes: 0,
      }
    }
  
  }
</script>

<style scoped>
  .header {
    font-size: 45px;
  }
  .outter-box {
    height: 20px;
    border: 1px solid #333;
    border-radius: 10px;
    background-color: #aaa;
    text-align: center;
  }
  .inner-box {
    width: 100%;
    height: 20px;
    border-radius: 10px;
    background-color: blue;
    color: white;
    
  }

</style>