<template>
  <div class="cards">
    <h2 class="name">{{ name }}</h2>
    <img :src="image" alt="" />
    <p>${{ cost }} | Calories: {{ cals }}</p>
    <p class="desc">{{ description }}</p>
    <AddtoCartButton @click="test"
      >Add {{ name }} to Cart ${{ cost }}</AddtoCartButton
    >
  </div>
</template>

<script>
import { pushScopeId } from "vue";
import AddtoCartButton from "./AddtoCart.vue";

export default {
  name: "Card",
  props: {
    name: String,
    cost: Number,
    cals: Number,
    image: String,
    description: String,
  },
  data() {
    return {
      totalofitem: 0,
      carts: [],
    };
  },
  components: {
    AddtoCartButton,
  },
  methods: {
    test() {
      this.$emit("added");
      this.$emit("omgplswork");
      this.carts.push(this.name);
      console.log(this.carts);
    },
  },
};
</script>

<style scoped>
.cards {
  width: 350px;
  background-color: rgb(125, 180, 125);
  text-align: center;
  padding: 15px;
  margin: auto;
  margin-bottom: 30px;
  border-radius: 50px;
  height: 370px;
}
img {
  width: 200px;
  border-radius: 50%;
}
h2 {
  font-size: 3vh;
}
.desc {
  margin-top: 10px;
}
.name {
  font-weight: bold;
}
</style>
