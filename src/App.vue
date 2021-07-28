  <template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <Counter />
    <ShowingParagraph />
    <Date />
    <HelloWorld msg="Welcome to Your Vue.js App" number="6" />
    <Component1 msg1="1" />
    <ListName />
    <ParentComponent />

    <ParentSend />
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

    ParentSend,
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
