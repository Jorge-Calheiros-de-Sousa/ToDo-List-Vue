<template>
  <div id="app">
    <to-do />
  </div>
</template>

<script>
import ToDo from "./main/ToDo.vue";
export default {
  name: "App",
  components: { ToDo },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
