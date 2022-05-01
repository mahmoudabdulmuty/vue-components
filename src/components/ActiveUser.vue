<template>
  <section>
    <h2>
      {{ username ? username : "no user detected" }}
    </h2>
    <h3>{{ age ? `${age} years old` : "" }}</h3>
  </section>
</template>

<script>
export default {
  props: {
    username: {
      type: String,
      required: true,
    },
    age: {
      type: Number,
      required: true,
    },
  },
};
</script>