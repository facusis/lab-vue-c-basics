
<script setup>
import { ref } from 'vue';

const myVar = ref('NavBar') 

const showVar = () => {
  return myVar.value
}

const ShowMenu = ref(false)

const toggleMenu = () => {
  ShowMenu.value = !ShowMenu.value
}

</script>

<template>
  <nav>
    <h3>Mi {{ showVar() }}</h3>
    <div class="container">
      <div class="div-menu" @click="toggleMenu">
        <img src="../assets/Images/Burger_menu.png" alt="Menu Logo">
        Menu
      </div>
      <ul v-show="ShowMenu" class="menu">
        <li><a href="#">Home</a></li>
        <li><a href="#">Contact</a></li>
        <li><a href="#">About Us</a></li>
      </ul>
    </div>
  </nav>
</template>

<style scoped>
  nav {
    background-color: cadetblue;
    padding: 2rem;
    text-align: center;
    display: flex;
    flex-direction: column;
    
  }

  .container {
    max-width: fit-content;
    
  }

  .menu {
    list-style: none;
    max-width: fit-content;
    padding: 0;
  }

  .menu li {
    background-color: darkslategray;
    padding: 0.5rem 1rem;
  }

  .menu a {
    text-decoration: none;
    color: black;
  }


  .div-menu {
    padding: 0.8rem 2rem;
    border: 1px solid black;
    border-radius: 15px;
    display: inline-flex;
    max-width: fit-content;
    color: black;
    margin-bottom: 0.5rem;

  }

  .div-menu:hover {
    cursor: pointer;
  }

  .div-menu img {
    margin: 0 1rem 0 0;
    
  }


</style>