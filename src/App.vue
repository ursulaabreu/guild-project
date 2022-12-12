<template>
  <ProductManagement />
</template>

<script>
import ProductManagement from './components/ProductManagement.vue';

export default {
  name: 'App',
  components: {
    ProductManagement,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
