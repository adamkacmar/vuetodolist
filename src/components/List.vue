<script>
import Item from "@/components/Item.vue";

export default {
  components: { 'to-do-item': Item },
  data() {
    return {
      items: [],
      newTask: '',
    };
  },
  methods: {
    addItem() {
      if (this.newTask.trim() !== '') {
        this.items.push({id: Date.now(), text: this.newTask});
        this.newTask = '';
      }
    },
    removeItem(id) {
      this.items = this.items.filter(item => item.id !== id);
    }
  }
}
</script>

<template>
  <div class="tasks-container">
    <to-do-item
      v-for="item in items"
      :key="item.id"
      :item="item"
      @remove="removeItem"
    ></to-do-item>
    <div class="input_container">
      <input v-model="newTask" @keyup.enter="addItem" class="todo_input" placeholder="Add new task...">
      <button @click="addItem" class="confirm_button">&#9658</button>
    </div>
  </div>
</template>

<style scoped>

</style>