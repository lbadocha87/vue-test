<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>
    <users-list />
  </div>
</template>

<script>

import UsersList from './components/UsersList.vue';
export default {
  components: { UsersList },
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
