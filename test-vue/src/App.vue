<template>
  <div id="app">
    <CanvasItem msg="Welcome to Your Vue.js App" />
    <p>{{ msg }}</p>
    <button v-on:click="btn()"></button>
  </div>
</template>

<script>
import CanvasItem from "./components/CanvasItem.vue";

export default {
  name: "App",
  components: {
    CanvasItem,
  },

  data: function () {
    return {
      msg: 123,
    };
  },

  methods: {
    btn: function () {
      this.msg = 321;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
