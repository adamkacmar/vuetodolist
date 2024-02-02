<script>
export default {
  props: ['item'],
}
</script>

<template>
  <div class="to_do_box">
    {{item.text}}
    <div class="button_container">
      <button @click="$emit('remove', item.id)" class="tick_button">&#10004</button>
      <button @click="$emit('remove', item.id)" class="cross_button">&#10006</button>
    </div>
  </div>
</template>

<style scoped>

</style>