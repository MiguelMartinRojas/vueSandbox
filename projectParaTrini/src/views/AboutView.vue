<template>
  <div class="about" >
    <h1>This is an about page with {{ name1 }} y {{ name2 }} numero: {{ count }}</h1>
  </div>

  
  <food-item
    v-for="x in foods"
    :key="x.name"
    :food-name="x.name"
    :food-desc="x.desc"
    :is-favorite="x.favorite">
  </food-item>
</template>


<script>
import { defineComponent } from 'vue'
import FoodItem from '../components/FoodItem.vue'


export default defineComponent({
  components: FoodItem,
  data() {
    let nombre1  = 'hola';
    nombre1 += " Trini";
    let nombre2  = 'hola';
    nombre2 = nombre2 + " Migue";

    return {
      count: 2,
      name1: nombre1,
      name2: nombre2,
      foods: [
        { name: 'Apples', desc: 'Apples are a type of fruit that grow on trees.', favorite: true},
        { name: 'Pizza', desc: 'Pizza has a bread base with tomato sauce, cheese, and toppings on top.', favorite: false},
        { name: 'Rice', desc: 'Rice is a type of grain that people like to eat.', favorite: false},
        { name: 'Fish', desc: 'Fish is an animal that lives in water.', favorite: true},
        { name: 'Cake', desc: 'Cake is something sweet that tastes good.', favorite: false}
      ],
    }
  },
  methods: {
 
  }
})

</script>

<style>
@media (min-width: 1024px) {
  .about {
    position: fixed;
    background-color: green;
    align-items: center;
  }
}
</style>
