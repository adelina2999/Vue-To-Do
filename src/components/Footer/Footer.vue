<template>
  <div>
    <button @click="increment">Increment</button>
    <p>Counter: {{ counter2 }}</p> 
    <p>Clicks: {{ clicks }}</p> 
  </div>
</template>

<script>
export default {
  name: 'Footer' ,
  data() {
    return {
      counter: 0,
      clicks: 0
    }
  },
  methods: {
    increment() {
      this.clicks++
    }
  },
  computed: {
    counter2() {
      return this.clicks * 2
    }
  }
}
</script>

<style>

</style>
