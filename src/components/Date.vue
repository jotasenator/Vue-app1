<template>
  <div>
    <button @click="handleDate">Obtain date!!</button>
    {{ date }}
  </div>
</template>

<script>
export default {
  name: "Date",
  data() {
    return {
      date: "",
    };
  },
  methods: {
    handleDate() {
      this.date = Date();
    },
  },
};
</script>

<style scoped>
</style>