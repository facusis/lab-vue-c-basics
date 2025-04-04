
<script setup>
  const props = defineProps({
    image: String,
    title: String,
    description: String,
    content: String
  
  })
</script>

<template>
  <div class="card">
    <h2>{{ title }}</h2>
    <img :src="image"  :alt="title">
    <h4>{{ description }}</h4>
    <p>{{ content }}</p>
  </div>
</template>


<style scoped>
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