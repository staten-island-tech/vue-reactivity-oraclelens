<template>
  <button><slot></slot></button>
</template>

<script>
export default {
  name: "AddtoCartButton",
  data() {
    return {};
  },
  props: {
    name: String,
    cost: Number,
  },
  methods: {},
};
</script>

<style scoped>
button {
  width: 200px;
  font-size: 15px;
  border: 10px white;
  border-radius: 50px;
  background-color: rgb(67, 103, 67);
  color: white;
  height: 50px;
  margin-top: 10px;
  transition: 0.5s;
  margin-bottom: 10px;
}
button:hover {
  transform: scale(1.2);
}
button:active {
  transform: scale(0.9);
}
</style>
