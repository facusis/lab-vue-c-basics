
<script setup>
  const currentYear = new Date().getFullYear() 
</script>

<template>
  <footer>
    <p>© {{ currentYear }} - Mi Sitio</p>
  </footer>
</template>

<style scoped>
  footer {
    background-color:rgb(19, 70, 70);
    padding: 2rem;
    text-align: center;
  }
</style>