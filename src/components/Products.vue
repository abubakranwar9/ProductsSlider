<template>
  <div>
    
      <div>
        <img v-bind:title="item.name" width="61" height="46" v-bind:src="item.productImageUrl" v-bind:alt="item.productImageAltText">
        <p>{{ item.name }}</p>
        <p>{{ item.code }}</p>
        <p>Stock : {{ item.salesUnit }}</p>
        <p>£{{ item.price.formattedValue }}</p>
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

<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
