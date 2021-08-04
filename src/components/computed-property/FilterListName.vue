<template>
  <div>
    <h3>Filter By Name</h3>
    <input type="text" v-model="name" placeholder="Filter By Name" />
    <ul>
      <li v-for="product in filterProductsByName" v-bind:key="product.id">
        Product Name : {{ product.name }} - Price : {{ product.price }} ({{
          product.category
        }})
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "FilterListName",
  data() {
    return {
      name: "",
      products: [
        { name: "Keyboard", price: 44, category: "Accessories" },
        { name: "Mouse", price: 20, category: "Accessories" },
        { name: "Monitor", price: 399, category: "Accessories" },
        { name: "Dell XPS", price: 599, category: "Laptop" },
        { name: "MacBook Pro", price: 899, category: "Laptop" },
        { name: "Pencil Box", price: 6, category: "Stationary" },
        { name: "Pen", price: 2, category: "Stationary" },
        { name: "USB Cable", price: 7, category: "Accessories" },
        { name: "Eraser", price: 2, category: "Stationary" },
        { name: "Highlighter", price: 5, category: "Stationary" },
      ],
    };
  },
  computed: {
    filterProductsByName() {
      return this.products.filter((x) => !x.name.indexOf(this.name));
    },
  },
};
</script>

<style scoped>
</style>