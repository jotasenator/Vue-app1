<template>
  <div>
    <ChildReceiving :numbers="numbers" @number-added="numbers.push($event)" />
  </div>
</template>

<script>
import ChildReceiving from "./ChildReceiving.vue";
export default {
  name: "ParentComponent",
  data() {
    return {
      numbers: [1, 2, 3],
    };
  },
  components: {
    ChildReceiving,
  },
};
</script>