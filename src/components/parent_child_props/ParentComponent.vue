<template>
  <div>
    <ChildComponent v-bind:numbers="dataNueva" />
  </div>
</template>

<script>
import ChildComponent from "./ChildComponent";

export default {
  name: "ParentComponent",
  data() {
    return {
      dataNueva: [12, 2, 3, 40, 5].sort((x, y) => x > y),
    };
  },
  components: {
    ChildComponent,
  },
};
</script>
