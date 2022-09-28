<template>
  <nav>

    <ul>
        <li href="">Link 1</li>
        <li href="">Link 2</li>
    </ul>
  </nav>

  <!-- Interaction 3 -->
  <div>
      
      <h2 v-show="interactionThree">La condición es verdadera</h2>
      
    </div>

    <br />
    <br />
    <!-- Interaction 5 -->
<div class="container" :class="changeColor ? 'is-red' : 'is-orange' ">
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Animi tempora quis assumenda maxime suscipit, cupiditate numquam dolorem placeat corrupti officia aliquid modi veniam molestias est? Aperiam sed amet eveniet ratione.</p>

    <button @click="changeColorFunction">Click Me to toogle color!</button>

</div>


</template>

<script setup>
import { ref } from "vue";

// Interaction 3
const interactionThree = ref(true); 


// Interaction 5

const changeColor = ref(true);
function changeColorFunction() {
    changeColor.value = !changeColor.value;
}

</script>

<style scoped>

.container{
    min-height: 20 rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.is-red{
    background-color: red;
}

.is-orange{
    background-color: orange;
}

p{
    color:black;
    text-align: center;
}


</style>