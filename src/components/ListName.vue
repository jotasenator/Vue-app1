<template>
  <div class="heroe">
    <h1>Heroes</h1>
    <ul>
      <li v-for="name in names" v-bind:key="name.id">
        {{ name }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "ListName",
  data() {
    return {
      names: [
        "Evan You",
        "John Lindquist",
        "Jen Looper",
        "Miriam Suzanne",
        "Chris Coyier",
        "Geoff Graham",
        "Divya Sasidharan",
        "Lea Verou",
        "Rachel Andrew",
        "Vitaly Friedman",
        "Ryan Florence",
        "Dan Abramov",
        "Jen Simmons",
        "Robin Rendle",
        "Nicole Sullivan",
      ],
    };
  },
};
</script>

<style scoped>
h1 {
  text-align: center;
  margin: 5px;
}

li {
  list-style: none outside none;
}
.heroe {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: left;
}
</style>