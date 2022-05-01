<template>
  <active-user :username="username" :age="userAge"></active-user>
  <user-data @set-user="setUser"></user-data>
</template>


<script>
import ActiveUser from "./components/ActiveUser.vue";
import UserData from "./components/UserData.vue";

export default {
  components: {
    ActiveUser,
    UserData,
  },
  data() {
    return {
      username: "",
      userAge: 0,
    };
  },
  methods: {
    setUser({ name, age }) {
      [this.username, this.userAge] = [name, +age];
    },
  },
};
</script>


<style>
html {
  font-family: sans-serif;
}
section {
  margin: 2rem auto;
  max-width: 40rem;
  border-radius: 12px;
  border: 1px solid #ccc;
  padding: 1rem;
}
</style>