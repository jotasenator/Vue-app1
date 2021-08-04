<template>
  <div>
    <hr />
    <h2>Shoping List</h2>

    <ul>
      <input
        class="form-control mb-5"
        v-model="newItem"
        name="newItem"
        placeholder="Add New Item"
        @keyup.enter="addItem"
      />
      <li
        class="list-group-item"
        v-for="item in items"
        :key="item.id"
        :class="{ removed: item.checked }"
      >
        <div class="form-check">
          <input
            class="form-check-input"
            type="checkbox"
            value=""
            v-model="item.checked"
          />
          <label class="form-check-label" for="defaultCheck1">
            {{ item.text }}
          </label>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "ShopingList",
  data() {
    return {
      items: [
        { text: "Banana", checked: false },
        { text: "Oranges", checked: false },
        { text: "Mangoes", checked: false },
      ],
      newItem: "",
    };
  },
  methods: {
    addItem() {
      let text;
      text = this.newItem.trim();
      if (text) {
        this.items.unshift({ text: this.newItem, checked: false });
        this.newItem = "";
      }
    },
  },
};
</script>

<style scoped>
.removed {
  color: gray;
}

.removed label {
  text-decoration: line-through;
}
</style>