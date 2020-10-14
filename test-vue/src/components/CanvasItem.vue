<template>
  <div class="canvas">
    <ul class="list">
      <li v-for="post in posts" v-bind:key="post.id">{{ post }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "CanvasItem",

  props: {
    msg: String,
  },

  data: function () {
    return {
      posts: ["item1", "item2", "item3"],
    };
  },
};
</script>

<style scoped>
  .list {
    
  }
</style>
