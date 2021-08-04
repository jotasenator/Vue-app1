<template>
  <div>
    <div id="app">
      <input type="text" v-model="name" />
      <input type="text" id="surname" value="Snow" />
      <button @click="saveSurname">Save Surname</button><br /><br />
      <output>{{ computedFullName }}</output>
    </div>
  </div>
</template>

<script>
let surname = "Snow";
export default {
  name: "ComputedCached",
  data() {
    return {
      name: "Jhon",
    };
  },
  computed: {
    computedFullName() {
      return this.name + "" + surname;
    },
  },
  methods: {
    saveSurname() {
      surname = this.$el.querySelector("#surname").value;
    },
  },
};
</script>

<style scoped>
</style>