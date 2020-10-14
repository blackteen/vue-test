<template>
  <div class="canvas">
    <ul class="list-group">
      <li class="list-group-item" v-for="post in posts" v-bind:key="post.id">{{ post }}</li>
    </ul>
    <button type="button" class="btn btn-primary" v-on:click="btn()">Revers List</button>
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
      posts: ["First item", "Second item", "Third item"],
    };
  },

   methods: {
    btn: function () {
      this.posts  = this.posts.reverse();
    },
  },

};
</script>

<style scoped>
  .list {
    list-style: none;
    padding: 0;
    margin: 0;
  }

  .list li {
    padding: 10px 5px;
    background: rgba(0,0,0,.2);
    margin: 0 0 10px;
  }
</style>
