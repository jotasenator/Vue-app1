<template>
  <div class="counter-buttons">
    <div>
      <button @click="handleAdd">Add</button>
      <button @click="handleReset">Reset</button>
      <button @click="handleSubstract">Substract</button>
    </div>
    {{ counter }}
  </div>
</template>

<script>
export default {
  name: "Counter",
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    handleAdd() {
      this.counter += 1;
    },
    handleReset() {
      if (this.counter !== 0) {
        this.counter = 0;
      }
    },
    handleSubstract() {
      this.counter -= 1;
    },
  },
};
</script>

<style scoped>
.counter-buttons {
  display: flex;
  justify-content: center;
  flex-direction: column;
}

button {
  width: 100px;
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
  font-size: 1rem;
  margin: 5px;
}
</style>