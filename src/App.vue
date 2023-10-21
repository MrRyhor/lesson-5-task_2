<template>
  <products-list :products-list-data="notebooksList"/>
</template>

<script>

import ProductsList from './components/ProductsList.vue'
import { notebooksList } from './constants/3_data_notebooks'

export default {
  name: 'App',
  components: {
    ProductsList    
  },

  data() {
    return {
      notebooksList,
    }
  },

}
</script>

<style>
#app {  
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  max-width: 600px;
  margin: 0 auto;
}
</style>
