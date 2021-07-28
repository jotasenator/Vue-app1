<template>
  <div class="input">
    <div>First name: <input type="text" v-model="name1" /></div>
    <div>Last name: <input type="text" v-model="name2" /></div>
    <button @click="handleAddUser">Add user</button>

    <p>el primer nombre es: {{ name1 }}</p>
    <p>El segundo nombre es {{ name2 }}</p>
    <table>
      <caption>
        Users
      </caption>
      <thead>
        <tr>
          <th>Index</th>
          <th>First name</th>
          <th>Last name</th>
        </tr>
      </thead>
      <tbody v-for="input in arrayInputs" v-bind:key="input.id">
        <tr>
          <td>{{ input.numero }}</td>
          <td>{{ input.name1 }}</td>
          <td>{{ input.name2 }}</td>
        </tr>
      </tbody>
    </table>
    <!-- <p>{{ arrayInputs }}</p> -->
  </div>
</template>

<script>
export default {
  name: "AddUsers",
  data() {
    return {
      name1: "",
      name2: "",
      arrayInputs: [],
      counter: 0,
    };
  },
  methods: {
    handleAddUser() {
      this.counter += 1;
      this.arrayInputs.push({
        numero: this.counter,
        name1: this.name1,
        name2: this.name2,
      });
      (this.name1 = ""), (this.name2 = "");
    },
  },
};
</script>

<style scoped>
.input {
  display: flex;
  flex-direction: column;
  align-items: center;
}
div {
  margin-bottom: 10px;
}
</style>