<template>
  <div id="header" class="structure-of-header">
    <Logo/>
    <div>
      <Welcome/>
      <Date/>
    </div>
    <Quote/>
    </div>
</template>

<script>
import Logo from './Logo'
import Welcome from './Welcome'
import Date from './Date'
import Quote from './Quote'

export default {
  name: 'Header',
  components: {
    Logo,
    Welcome,
    Date,
    Quote
  }
}
</script>

<style>
  .structure-of-header {
    overflow: hidden;
    background-color: #f1f1f1;
    padding: 20px 10px;
  }
</style>
