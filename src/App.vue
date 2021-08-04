  <template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <AddUsers />
    <Counter />
    <ShowingParagraph />
    <Date />
    <HelloWorld msg="Welcome to Your Vue.js App" number="6" />
    <Component1 msg1="1" />
    <ListName />
    <ParentComponent />
    <InputName />
    <ParentSend />
    <FilterListName />
    <FilterPriceRange />
    <FilterList />
    <ComputedCached />
    <InputBinding />
    <TogglePassVisibility />
    <ShowLess />
    <TipCalculator />
    <ShopingList />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Component1 from "./components/Component1.vue";
import ListName from "./components/ListOfNames.vue";
import Counter from "./components/Counter.vue";
import Date from "./components/Date.vue";
import ShowingParagraph from "./components/ShowingP.vue";
import ParentComponent from "./components/parent_child_props/ParentComponent.vue";
import ParentSend from "./components/child_parent_props/ParentSend.vue";
import AddUsers from "./components/test-dome-addUsers/AddUsers.vue";
import InputName from "./components/computed-property/InputName.vue";
import FilterList from "./components/computed-property/FilterListCategory.vue";
import FilterListName from "./components/computed-property/FilterListName.vue";
import FilterPriceRange from "./components/computed-property/FilterPriceRange.vue";
import ComputedCached from "./components/computed-property/ComputedCached.vue";
import InputBinding from "./components/input-binding/InputBinding.vue";
import TogglePassVisibility from "./excercices/TogglePassVisibility.vue";
import ShowLess from "./excercices/ShowLess.vue";
import TipCalculator from "./excercices/TipCalculator.vue";
import ShopingList from "./excercices/ShopingList.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    Component1,
    ListName,
    Counter,
    Date,
    ShowingParagraph,
    ParentComponent,
    AddUsers,
    ParentSend,
    InputName,
    FilterList,
    FilterListName,
    FilterPriceRange,
    ComputedCached,
    InputBinding,
    TogglePassVisibility,
    ShowLess,
    TipCalculator,
    ShopingList,
  },
};
</script>>

<style >
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
