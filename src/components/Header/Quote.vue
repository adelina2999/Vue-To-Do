<template>
  <div>
    <header>
      <blockquote>
      <cite>{{ getRandomQuoteAndAuthor().quote }}</cite>
      - {{ getRandomQuoteAndAuthor().author }}</blockquote>
    </header>
  </div>
</template>

<script>4
import quoteJSON from '../../JSON/Quotes.json'

export default {
  name: 'Quote',
  data() {
    return {
    }
  },
  methods: {
    getRandomQuoteAndAuthor() {
      let randomNumber = Math.floor(Math.random() * (quoteJSON.quotes.length))
      
      return {
        author: quoteJSON.quotes[randomNumber].author,
        quote: quoteJSON.quotes[randomNumber].quote
      }
    }
  }
}
</script>

<style>

</style>
