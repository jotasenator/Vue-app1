<template>
  <div>
    <p>your name is: {{ name }}</p>
    <p>Your name has a length of: {{ lengthName }}</p>
    <input type="text" v-model="name" />
  </div>
</template>

<script>
export default {
  name: "Input",
  data() {
    return {
      name: "",
    };
  },
  computed: {
    lengthName() {
      return this.name.length;
    },
  },
};
</script>

<style scoped>
</style>