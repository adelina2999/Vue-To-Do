<template>
  <div id="shopping-list">
    <h1>{{ header.toLocaleUpperCase() }}</h1>
    <div class="add-item-form">
            <!-- @keyup.enter adauga elemente din input prin enter -->
      <input 
        v-model="newItem" type="text" 
        placeholder="Add an item" 
        @keyup.enter="items.push(newItem)">
      <button class="btn btn-primary" @click="items.push(newItem)">Save Item</button>
    </div>
    <ul>
      <li v-for="item in items" 
        :key="item">{{ item }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Content',
  data() {
    return {
      header: 'Shopping List App',
      newItem: '',
      items: [
        '10 party hats',
        '2 board games',
        '20 cups'
      ]
    }
  }
}
</script>

<style>

</style>
