<template>
  <div id="app">
    <h2>Related Products</h2>
    <vue-glide
      type="carousel"
      :per-view="4"
      :autoplay="5000"
      :animationDuration="1000"
      :breakpoints="{
        1200: {
          perView: 3
        },
        700: {
          perView: 2
        }
      }"
    >
      <vue-glide-slide
        class="glide__slide"
        v-for="item in items.carouselData"
        :key="item.code"
      >
        <Products v-bind:item="item" />
      </vue-glide-slide>
    </vue-glide>
  </div>
</template>

<script>
import Products from "./components/Products.vue";
import items from "./data.json";
import { Glide, GlideSlide } from "vue-glide-js";

export default {
  name: "app",
  data: function() {
    return {
      items: items,
      perView: 4
    };
  },
  components: {
    Products,
    [Glide.name]: Glide,
    [GlideSlide.name]: GlideSlide
  }
};
</script>

<style lang="sass">
@import "../node_modules/vue-glide-js/dist/vue-glide.css";
#app
  font-family: "Avenir", Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-align: center
  color: #2c3e50
  margin-top: 60px
  .glide
    border: 1px solid #eaeaea
    padding: 10px
    box-shadow: 5px 10px #eaeaea
  .glide__slide
    border-right: 1px solid #eaeaea
</style>
