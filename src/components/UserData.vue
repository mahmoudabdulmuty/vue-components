<template>
  <section>
    <form @submit.prevent="setUser">
      <input type="text" placeholder="Your name" v-model="name" />
      <input type="number" placeholder="Your age" v-model="age" />
      <button>Set User</button>
    </form>
  </section>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      age: "",
    };
  },
  emits: ["set-user"],
  methods: {
    setUser() {
      const newUser = {
        name: this.name,
        age: this.age,
      };
      this.$emit("set-user", newUser);
      [this.name, this.age] = ["", ""];
    },
  },
};
</script>

