<template>
  <div id="header">
    <Welcome/>
    <Date/>
    <Quote/>
    </div>
</template>

<script>
import Welcome from './Welcome'
import Date from './Date'
import Quote from './Quote'

export default {
  name: 'Header',
  components: {
    Welcome,
    Date,
    Quote
  }
}
</script>

<style>

</style>