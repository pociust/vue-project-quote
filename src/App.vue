<template>
  <div>
    <QuotesBar></QuotesBar>
    <QuoteInputText></QuoteInputText>
    <Footer></Footer>
  </div>
</template>

<script>
import QuotesBar from './components/QuotesBar';
import QuoteInputText from './components/QuoteInputText';
import Footer from './components/Footer';

  export default {
    components: {
      QuotesBar,
      QuoteInputText,
      Footer
    }
  }
</script>