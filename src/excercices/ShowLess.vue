<template>
  <div>
    <hr />
    <div class="col-md-8 mx-auto">
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum iste
        <span v-show="!more">...</span>
        <span v-show="more"
          >iusto magni voluptas impedit vitae neque aut eaque repudiandae
          laboriosam in, minima totam animi sunt aliquam? Architecto at esse
          labore?</span
        >
      </p>
      <button @click="toggleText" class="btn btn-primary my-3">
        {{ buttonText }}
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ShowLess",
  data() {
    return {
      more: false,
    };
  },
  methods: {
    toggleText() {
      this.more = !this.more;
    },
  },
  computed: {
    buttonText() {
      return this.more ? "Show less" : "Show more";
    },
  },
};
</script>

<style scoped>
p {
  text-align: left;
}
button {
  display: flex;
  justify-content: left;
}
</style>