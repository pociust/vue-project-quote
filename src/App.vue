<template>
  <div>
    <QuotesBar></QuotesBar>
    <QuoteInputText></QuoteInputText>
    <Quotes></Quotes>
    <Footer></Footer>
  </div>
</template>

<script>
import QuotesBar from './components/QuotesBar';
import QuoteInputText from './components/QuoteInputText';
import Quotes from './components/Quotes';
import Footer from './components/Footer';

  export default {
    components: {
      QuotesBar,
      QuoteInputText,
      Quotes,
      Footer
    }
  }
</script>