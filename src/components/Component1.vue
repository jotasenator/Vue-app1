<template>
  <div>
    <h2>Como esta la timba</h2>
    <h3>Este es mi {{ msg1 }} componente</h3>
  </div>
</template>

<script>
export default {
  name: "Component1",
  props: {
    msg1: Number,
  },
};
</script>

<style scoped>
h2 {
  color: red;
}
h3 {
  color: blue;
}
</style>