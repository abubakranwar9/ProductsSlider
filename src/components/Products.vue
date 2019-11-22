<template>
  <div>
    <div>
      <img
        class="image--product-display"
        v-bind:title="item.name"
        v-bind:src="item.productImageUrl"
        v-bind:alt="item.productImageAltText"
      />
      <p>{{ item.name }}</p>
      <p>Code: {{ item.code }}</p>
      <p>Stock : {{ item.salesUnit }}</p>
      <b>Price £{{ item.price.formattedValue }}</b>
      <a class="button--product-advance" v-bind:href="item.url">View Product</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Products",
  props: {
    item: Object
  }
};
</script>
<style lang="sass">
.image--product-display
  width: 200px
.button--product-advance
  display: block
  width: 150px
  text-decoration: none
  background: #4E9CAF
  margin: auto
  margin-top: 10px
  padding: 10px
  text-align: center
  border-radius: 5px
  color: white
  font-weight: bold
</style>
