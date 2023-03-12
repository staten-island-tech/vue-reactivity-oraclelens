<script>
import Card from '../components/Card.vue';
import AddtoCartButton from '../components/AddtoCart.vue';

export default{
  name: "Menu",
  components: {
    Card,
    AddtoCartButton,
  },
  data(){
    return{
      foods: [
        {
          name: "Shack Burger",
          cost: 6.89,
          cals: 500,
          image: "https://d2luv1saso99wi.cloudfront.net/2022_Digital-Menu_Burgers_ShackBurger_1500x920_lg1663589553.jpeg",
          description: "Angus beef cheeseburger with lettuce, tomato, and ShackSauce on a toasted potato bun",
        },
        {
          name: "Shroom Burger",
          cost: 8.69,
          cals: 510,
          image: "https://d2luv1saso99wi.cloudfront.net/2022_Digital-Menu_Burgers_ShroomBurger_1500x920_lg1663589675.jpeg",
          description: "Crisp-fried portobello mushroom filled with melted muenster and cheddar cheeses, with lettuce, and tomato on a toasted potato bun",
        },
        {
          name: "Smoke Shack",
          cost: 8.49,
          cals: 570,
          image: "https://d2luv1saso99wi.cloudfront.net/2022_Digital-Menu_Burgers_SmokeShack_1500x920_lg1663589622.jpeg",
          description: "Angus beef cheeseburger with applewood-smoked bacon, chopped cherry peppers, and ShackSauce on a toasted potato bun",
        },
        {
          name: "Chicken Shack",
          cost: 8.29,
          cals: 550,
          image: "https://d2luv1saso99wi.cloudfront.net/2022_Digital-Menu_Chicken_ChickenShack_1500x920_lg1663591157.jpeg",
          description: "Crispy, white-meat chicken breast over lettuce, pickles, and buttermilk herb mayo on a toasted potato bun",
        },
      ]
    }
  }
}
</script>

<template>
  <main>
    <div class="menu">
      <Card v-for="food in foods" 
      :key="food.name" 
      :name="food.name" 
      :cost="food.cost"
      :image="food.image"
      :description="food.description"
      :cals="food.cals"/>    
    </div>
  </main>
</template>

<style scoped>
  .menu{
    display: flex;
    flex-wrap: wrap; 
    justify-content:space-evenly;
  }
  *{
    color:black
  }
</style>
