<template>
  <div id="app">
    <menu-dropdown></menu-dropdown>
    <menu-dropdown></menu-dropdown>
    <menu-dropdown></menu-dropdown>
  </div>
</template>

<script>
import MenuDropdown from "@/components/MenuDropdown.vue";

export default {
  name: "app",
  components: {
    MenuDropdown
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
