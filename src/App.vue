<template>
  <div class="p-10">
    <QuotesBar :progressBar="quotes.length"></QuotesBar>
    <QuoteInputText @singleQuoteToPush="quotes.push($event)" :quoteLengthLimitation="quotes.length"></QuoteInputText>
    <Quotes>
      <div class="frow">
        <div v-for="quote in quotes" :key="quote.length" class="row-between shadow-light p-10 m-10">
            <p>{{ quote }}</p>
        </div>
      </div>
    </Quotes>
    <Footer></Footer>
  </div>
</template>

<script>
import QuotesBar from './components/QuotesBar';
import QuoteInputText from './components/QuoteInputText';
import Quotes from './components/Quotes'
import Footer from './components/Footer';

  export default {
    data() {
      return {
        quotes: [],
      }
    },
    components: {
      QuotesBar,
      QuoteInputText,
      Quotes,
      Footer
    }
  }
</script>