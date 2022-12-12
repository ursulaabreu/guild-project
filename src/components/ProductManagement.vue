<template>
  <input type="text" v-model="name" />

  <input type="text" v-model="description" />

  <select v-model="type">
    <option v-for="option in typeOptions" :value="option" :key="option">
      {{ option }}
    </option>
  </select>

  <input type="number" v-model="stock" />

  <button @click="addProduct()">Add Product</button>

  <div v-for="product in products" :key="product.name">
    <ProductItem :item="product"></ProductItem>
  </div>
</template>

<script>
import ProductItem from './ProductItem.vue';

export default {
  name: 'ProductManagement',
  data() {
    return {
      products: [
        {
          name: 'Product 1',
          description: 'Im a toy product',
          type: 'TOY',
          stock: 10,
        },
        {
          name: 'Product 2',
          description: 'Im a clothes product',
          type: 'CLOTHES',
          stock: 1,
        },
      ],
      name: '',
      description: '',
      type: null,
      stock: '',
      typeOptions: ['TOY', 'CLOTHES'],
    };
  },
  methods: {
    addProduct() {
      this.products.push({
        name: this.name,
        description: this.description,
        type: this.type,
        stock: this.stock,
      });

      this.name = '';
      this.description = '';
      this.type = null;
      this.stock = '';
    },
  },
  components: {
    ProductItem,
  },
};
</script>

<style scoped></style>
