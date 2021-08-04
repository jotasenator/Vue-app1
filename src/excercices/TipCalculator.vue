<template>
  <div>
    <hr />
    <h2 class="aligned-left">Tip Calculator</h2>
    <form>
      <div class="form-group aligned-left">
        <label for="name">How much is the total Bill Amount: ?</label>
        <input
          type="number"
          class="form-control"
          id="amount"
          placeholder="Total Bill Amount"
          v-model="amount"
        />
      </div>

      <div class="form-group aligned-left">
        <label for="exampleFormControlSelect2">How was the service: ?</label>
        <select class="form-control" id="service" v-model="service">
          <option value="30">30%(Exceptional)</option>
          <option value="25">25%(More than good)</option>
          <option value="20">20%(Good)</option>
          <option value="15">15%(It was OK)</option>
          <option value="10">10%(Bad)</option>
          <option value="5">5%(Terrible)</option>
        </select>
      </div>

      <div class="form-group aligned-left">
        <label for="name">How many people are sharing the bill: ?</label>
        <input
          type="number"
          class="form-control"
          id="sharing"
          placeholder="Total Bill Amount"
          v-model="sharing"
        />
      </div>
      <p class="alert alert-success aligned-left" role="alert">
        Tip amount:${{ tipFunction() }}/per person
      </p>
    </form>
  </div>
</template>

<script>
export default {
  name: "TipCalculator",
  data() {
    return {
      amount: "",
      service: "",
      sharing: 1,
    };
  },
  methods: {
    tipFunction() {
      if (
        !isNaN(this.amount) &&
        this.amount > 0 &&
        this.service !== "" &&
        this.sharing > 0
      ) {
        return (((this.amount / this.sharing) * this.service) / 100).toFixed(2);
      } else {
        return (0).toFixed(2);
      }
    },
  },
};
</script>

<style scoped>
.aligned-left {
  text-align: left;
}
</style>