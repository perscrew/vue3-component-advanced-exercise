<template>
  <user-list></user-list>
</template>

<script>
import UserList from './components/user/UserList.vue';

export default {
  name: 'App',
  provide() {
    return { users: this.users };
  },
  components: {
    UserList,
  },
  data() {
    return {
      users: [
        { id: 0, firstName: 'Thibaud', lastName: 'Dervily', age: 39 },
        { id: 1, firstName: 'Marco', lastName: 'Polo', age: 34 },
        { id: 2, firstName: 'Hubert', lastName: 'Dupont', age: 23 },
        { id: 3, firstName: 'David', lastName: 'Luby', age: 46 },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
