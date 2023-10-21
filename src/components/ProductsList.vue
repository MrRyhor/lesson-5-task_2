<template>
  <div class="container">
    <product-item
      v-for="product in productsListData"
      :key="product.id"
      :item-data="product"
    />
  </div>
</template>
<script>
import ProductItem from "./ProductItem.vue";

export default {
  components: { ProductItem },
  name: "ProductsList",

  props: {
    productsListData: {
      type: Array,
      default: () => [],
    },
  },
};
</script>
<style lang="css" scoped>
.container {
    margin-top: 10px;
    
}
</style>
