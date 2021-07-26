  <template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" number="6" />
    <Component1 msg1="1" />
    <ListName />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Component1 from "./components/Component1.vue";
import ListName from "./components/ListName.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    Component1,
    ListName,
  },
};
</script>

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
