<script>
import TheWelcome from "../components/TheWelcome.vue";

export default {
  name: "Home",
  component: {},
  data() {
    return {
      student: "help, i am so bad at algebra 2",
      graduated: false,
    };
  },
};
</script>

<template>
  <main>
    <h1 v-if="graduated">{{ student }}</h1>
    <h1 v-else="graduated">loser</h1>
  </main>
</template>
