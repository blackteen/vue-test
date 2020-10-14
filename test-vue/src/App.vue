<template>
  <div id="app">
    <CanvasItem />
    <p>{{ message  }}</p>
    <button type="button" class="btn btn-primary" v-on:click="btn()">Revers Text</button>
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
      message : "Hello World",
    };
  },

  methods: {
    btn: function () {
      this.message  = this.message.split('').reverse().join('');
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
}
</style>
