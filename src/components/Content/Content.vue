<template>
  <div id="shopping-list">
    <div>
      <h1>{{ header.toLocaleUpperCase() }}</h1>
      <button v-if="state === 'default'" class="btn btn-primary" @click="changeState('edit')">Add item</button>
      <button v-else class="btn btn-cancel" @click="changeState('default')">Cancel</button>
    </div>
    <div v-if="state === 'edit'" class="add-item-form">
      <input 
        v-model="newItem" type="text" 
        placeholder="Add an item" 
        @keyup.enter="saveItem">
      <button class="btn btn-primary" :disabled="newItem.length === 0" @click="items.push(newItem)">Save Item</button>
    </div>
    <ul>
      <li v-for="item in items" 
        :key="item"
        :class="[item.purchased ? 'strikeout' : '', item.highPriority ? 'priority' : '']">{{ item.label }}</li>
    </ul>
    <p v-if="items.length === 0">Nice job! You've bough all your items</p>
  </div>
</template>

<script>
export default {
  name: 'Content',
  data() {
    return {
      state: 'default',
      header: 'Shopping List App',
      newItem: '',
      items: [
        {
          label: '2 board games',
          purchased: true,
          highPriority: false,
        },
        {
          label: '20 cups',
          purchased: false,
          highPriority: true,
        },
        {
          label: '10 party hats',
          purchased: false,
          highPriority: false,
        }
      ]
    }
  },
  methods: {
    saveItem() {
      this.items.push({
          label: this.newItem,
          purchased: false,
        },)
      this.newItem = ''
    },
    changeState(newState) {
      this.state = newState
      this.newItem = ''
            
    }
  }
}
</script>

<style>

</style>
