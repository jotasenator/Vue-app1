<template>
  <div class="paragraph">
    <hr />
    <a href="#" @click="handleState">Click me</a>
    <p v-if="state">
      Este parrafo debe no mostrarse y despues si, y despues no
    </p>
    <hr />
  </div>
</template>

<script>
export default {
  name: "ShowingParagraph",
  data() {
    return {
      state: false,
    };
  },
  methods: {
    handleState() {
      this.state = !this.state;
    },
  },
};
</script>

<style scoped>
p {
  background-color: pink;
}
</style>