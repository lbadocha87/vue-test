<template>
  <div class="hello">
    <h1>{{ counter }}</h1>
    <button v-on:click="add">Add 1</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      counter: 1
    }
  },

  methods: {
    add: function () {
      this.counter = this.counter + 1;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
