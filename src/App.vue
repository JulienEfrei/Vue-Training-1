<template>
  <div>
  <Card 
  v-for="item in items"
  :name = "item.name"
  :price = "item.price"
  :image = "item.image"
  :isCold = "item.isCold"
  :key="item"
  />
</div>
</template>
<script setup>
import Card from "./components/card.vue";
const image="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c5/Roasted_coffee_beans.jpg/1200px-Roasted_coffee_beans.jpg";
const items =[{
  name: 'Vanilla Latte',
  price: 4.99,
  isCold: false,
  image : image,
}
, {
  name: 'Iced Coffee',
  price: 3.99,
  isCold: true,
  image : image,
},
{
  name: 'Cappuccino',
  price: 5.99,
  isCold: false,
  image : image,
},
{
  name: 'Iced Tea',
  price: 2.99,
  isCold: true,
  image : image,
}
]

</script>


<style scoped>

</style>
