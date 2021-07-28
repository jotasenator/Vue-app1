<template>
  <div>
    <h2>numbers es este array:--> {{ numbers }}</h2>
    <input v-model="number" type="number" />
    <button @click="$emit('number-added', Number(number))">
      Add new number
    </button>
  </div>
</template>

<script>
export default {
  name: "ChildReceiving",
  props: {
    numbers: Array,
  },
  data() {
    return {
      number: 0,
    };
  },
};
</script>