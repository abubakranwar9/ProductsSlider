<template>
  <div id="app">
    <li v-for="item in items.carouselData" :key="item.code">
      <Products v-bind:item="item" />
    </li>
  </div>
</template>

<script>
import Products from "./components/Products.vue";
import items from "./data.json";

export default {
  name: "app",
  data: function() {
    return {
      items: items
    };
  },
  components: {
    Products
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
