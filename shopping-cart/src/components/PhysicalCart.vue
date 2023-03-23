<template>
  <div class="cart">
    <Cart
      v-for="cart in carts"
      :key="cart.name"
      :name="cart.name"
      :cost="cart.cost"
      @test="additemspls"
    />
  </div>
</template>

<script>
import CartButton from "../components/CartButton.vue";
import Cart from "../components/Cart.vue";

export default {
  name: "PhysicalCart",
  components: {
    CartButton,
    Cart,
  },
  data() {
    return {};
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
