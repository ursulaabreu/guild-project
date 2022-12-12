<template>
  <!-- v-model is a directive that creates a two-way data binding between a value in our template and a value in our data properties -->
  <input type="text" v-model="name" />

  <input type="text" v-model="description" />

  <select v-model="type">
    <!-- v-for is a directive used to loop over a data usually an array -->
    <option v-for="option in typeOptions" :value="option" :key="option">
      <!-- The most basic form of data binding is text interpolation using the “Mustache” syntax (double curly braces) -->
      {{ option }}
    </option>
  </select>

  <input type="number" v-model="stock" />

  <!-- Listen to DOM events and run some JavaScript when they're triggered -->
  <button @click="addProduct()">Add Product</button>
</template>

<script>
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
};
</script>

<style scoped></style>
