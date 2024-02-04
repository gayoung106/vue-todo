<template>
  <div class="name">{{ name }}</div>
  <button class="btn btn-primary" v-on:click="updateName">Click</button>
  <div>{{ greeting(name) }}</div>
  <div>{{ greet }}</div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const name = ref("gayoung");

    const greeting = (name) => {
      return "Hello, " + name;
    };

    const greet = greeting(name);

    const updateName = () => {
      name.value = "gayoung2";
      console.log(name);
    };

    return {
      name,
      greeting,
      greet,
      updateName,
    };
  },
};
</script>

<style>
.name {
  color: blue;
}
</style>
