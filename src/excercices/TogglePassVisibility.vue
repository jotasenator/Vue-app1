<template>
  <div>
    <br /><br />
    <hr />
    <div class="input-group mb-3">
      <input
        class="form-control"
        placeholder="Password"
        :type="[type ? 'password' : 'text']"
      />
      <div class="input-group-append">
        <span class="input-group-text"
          ><i
            :class="[!type ? 'fa fa-eye' : 'fa fa-eye-slash']"
            aria-hidden="true"
            @click="handleClick"
          ></i
        ></span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TogglePassVisibility",
  data() {
    return {
      type: true,
    };
  },
  methods: {
    handleClick() {
      this.type = !this.type;
    },
  },
};
</script>

<style scoped>
</style>