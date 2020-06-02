<template>
  <div>
    <input type="text" @input="cssClass = 
    $event.target.value">
    <p :class="cssClass">Class: {{ cssClass }}</p> 
  </div>
</template>

<script>
export default {
  name: 'Footer' ,
  data() {
    return {
      cssClass: ''
    }
  }
}
</script>

<style>
  .red {
    background-color: red;
  }

  .blue {
    background-color: royalblue;
  }
</style>
