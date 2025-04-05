
<script setup>
  const props = defineProps({
    image: String,
    title: String,
    description: String,
    content: String,
    bgColor:String,
    changeBgColor: Function
  
  })

</script>

<template>
  <button class="button" @click="changeBgColor">Change color</button>
  <div class="card" :style="{ backgroundColor: bgColor }">
    <h2>{{ title }}</h2>
    <img :src="image"  :alt="title">
    <h4>{{ description }}</h4>
    <p>{{ content }}</p>
  </div>
</template>


<style scoped>

  .button {
    padding: 0.5rem 1rem;
    background-color: darkcyan;
  }

  .card {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    justify-content: center;
    align-items: center;
    padding: 2rem;
  }

  .card img {
    width: 20rem;
    height: 30rem;
  }

  .card h2 {
    font-size: 5rem;
  }

  .card p {
    font-size: 1.5rem;
  }
</style>