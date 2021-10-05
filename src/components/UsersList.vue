<template>
  <div>
    <h2>users list</h2>
    <form v-on:submit="add">
      <input type="text" v-model="inputValue"/>
      <button>add</button>
    </form>
    <ul>
      <li v-for="user in users" v-on:click="remove">{{ user }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "UsersList",
  data() {
    return {
      users: ["Adam", "Ola", "Kasia"],
      inputValue: ''
    };
  },

  methods: {
    add: function (e) {
      e.preventDefault();
      this.users = this.users.concat(this.inputValue);
    },
    remove: function(e) {
        this.users = this.users.filter(user=> {
            return user !== e.target.textContent;
        })
    }
  },
};
</script>