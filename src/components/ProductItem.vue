<template>
  <div class="container">
    <a :href="itemData.link" target="_blank">
      <div class="image-container">
        <img :src="itemData.imgSrc" alt="product" />
      </div>
    </a>
    <div class="content-container">
      <a :href="itemData.link" target="_blank">
        <h3>{{ itemData.title }}</h3>
      </a>
      <p>
        Discount: <span>{{ itemData.discount }} &#8372;</span>
      </p>
      <h4>{{ itemData.oldPrice }} &#8372;</h4>
      <div class="price-container">
        <h1>{{ itemData.price }} &#8372;</h1>
        <button type="button">Buy</button>
      </div>
    </div>    
  </div>
</template>
<script>
export default {
  name: "ProductItam",
  props: {
    itemData: {
      type: Object,
      default: () => ({}),
    },
  },
};
</script>
<style lang="css" scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
a {
    text-decoration: none;
    color: blue;
}
span {
    color: red;
}
h4 {
    text-decoration: line-through;
    color: rgb(137, 137, 137);
}
.container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  border: 2px solid teal;
  padding: 10px;
}
.image-container {

}
.image-container img {
    width: 200px;
}
.content-container {
    margin-left: 55px;
  display: flex;
  flex-direction: column;
  text-align: left;
  gap: 10px;
}
.price-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
h1 {
    color: red;
}
button {
    padding: 10px 30px;
    background-color: rgb(21, 227, 158);
    color: #fff;
    border-radius: 5px;
    border: none;
    cursor: pointer;
}
</style>
