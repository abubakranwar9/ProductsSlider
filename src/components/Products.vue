<template>
  <div>
    <div>
      <img
        class="product-images"
        v-bind:title="item.name"
        v-bind:src="item.productImageUrl"
        v-bind:alt="item.productImageAltText"
      />
      <p>{{ item.name }}</p>
      <p>Code: {{ item.code }}</p>
      <p>Stock : {{ item.salesUnit }}</p>
      <b>Price £{{ item.price.formattedValue }}</b>
      <a class="product-link" v-bind:href="item.url">View Product</a>
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
.product-images
  width: 200px
.product-link
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
