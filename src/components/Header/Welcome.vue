<template>
  <div> 
    <h3 class="welcome-align example">Welcome to my page</h3>
  </div> 
</template>

<script>
export default {
    
}
</script>

<style>
  .welcome-align {
    position: absolute;
    top: 5px;
    right: 5px;
    text-align: right;
  }

  @media all and (min-width: 250px) {
    .example {
      font-size: 30px;
    }
  }

  @media all and (max-width: 249px) {
    .example {
      font-size: 10px
    }
  }
</style>
