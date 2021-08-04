<template>
  <div>
    <h3>Filter By Price Range</h3>
    <label for="vol">Price (between 0 and 1000):</label>
    <input type="range" v-model="range" min="0" max="1000" step="10" />
    Selected : {{ range }}
    <ul>
      <li v-for="product in filterProductsByRange" v-bind:key="product.id">
        Product Name : {{ product.name }} - Price : {{ product.price }} ({{
          product.category
        }})
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "FilterPriceRange",
  data() {
    return {
      range: "",
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
    filterProductsByRange() {
      return this.products.filter((x) =>
        x.price > 0 && x.price < this.range ? x : ""
      );
    },
  },
};
</script>

<style scoped>
</style>