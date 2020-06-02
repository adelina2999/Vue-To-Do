<template>
  <div>
    <button v-on:click="changeTitle">Change Title</button>   
    <p>{{ title }}</p> 
  </div>
</template>

<script>
export default {
  name: 'Footer' ,
  data() {
    return {
      title: 'Hello World!'
    }
  },
  methods: {
    changeTitle() {
      this.title = 'New Title'
    }
  },
}
</script>

<style>

</style>
