<template>
  <div class="name">{{ name }}</div>
  <div>{{ greeting(name) }}</div>
  <div>{{ greet }}</div>
</template>

<script>
export default {
  setup() {
    const name = "gayoung";

    const greeting = (name) => {
      return "Hello, " + name;
    };

    const greet = greeting(name);

    return {
      name,
      greeting,
      greet,
    };
  },
};
</script>

<style>
.name {
  color: blue;
}
</style>
