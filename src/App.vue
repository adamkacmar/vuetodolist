<template>
  <div class="box">
    <Header></Header>
    <List></List>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import List from "@/components/List.vue";

export default {
  name: 'App',
  components: {
    List,
    Header,
  }
}
</script>

<style>
/* Global styles (if any) */
</style>