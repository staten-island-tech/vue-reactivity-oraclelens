<template>
  <div class="cart">
    <ul>
      <li v-for="store in store">
        {{ cart }}
      </li>
    </ul>
  </div>
</template>

<script>
import CartButton from "../components/CartButton.vue";
import Cart from "../components/Cart.vue";
import { store } from "./store.js";

export default {
  name: "PhysicalCart",
  components: {
    CartButton,
    Cart,
  },
  data() {
    return {
      store,
    };
  },
  props: {
    name: String,
    cost: Number,
    cals: Number,
  },
  methods: {},
};
</script>

<style scoped>
.cart {
  width: 700px;
  background-color: rgb(148, 148, 148);
  text-align: center;
  padding: 15px;
  margin: auto;
  margin-bottom: 30px;
  border-radius: 50px;
}
</style>
