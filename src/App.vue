
<script setup>
  import Navbar from '../src/components/Navbar.vue'
  import Footer from '../src/components/Footer.vue'
  import Cards from '../src/components/Cards.vue'

  import { ref } from 'vue'

  const cards = ref([
    {
      image: '/src/assets/Images/gorila.png',
      title: 'Gorila',
      description: 'Un gorila es un gran primate, de complexión robusta, nativo de las selvas de África.',
      content: 'El gorila es uno de los animales más fuertes del planeta y, a pesar de su tamaño imponente, es muy pacífico y social. Se encuentra en bosques tropicales y montañas de África central, y su dieta se basa principalmente en frutas, hojas y tallos. Los gorilas viven en grupos dirigidos por un macho dominante llamado "espalda plateada", y su comportamiento refleja una estructura social compleja. Estos primates son inteligentes, tienen la capacidad de utilizar herramientas y mostrar emociones similares a las humanas.'
    },
    {
      image: '/src/assets/Images/perro.png',
      title: 'Perro',
      description: 'El perro es un mamífero doméstico, conocido por su lealtad y diversidad de razas.',
      content: 'El perro es considerado el mejor amigo del hombre por su capacidad para formar fuertes lazos con los humanos. Hay más de 300 razas de perros, y pueden variar enormemente en tamaño, forma, color y temperamento. Son excelentes compañeros y pueden ser entrenados para diversas tareas, como la asistencia a personas con discapacidades, la búsqueda y rescate, o el pastoreo. Los perros también tienen un agudo sentido del olfato, y algunos son empleados en labores de detección de sustancias, como drogas o explosivos.'
    },
    {
      image: '/src/assets/Images/tucan.png',
      title: 'Tucan',
      description: 'El tucán es un ave tropical conocida por su gran pico colorido y su canto melodioso.',
      content: 'El tucán es nativo de América Central y del Sur, y es famoso por su característico pico grande y brillante, que le ayuda a alcanzar frutas en árboles altos. A pesar de su tamaño, el pico es ligero debido a su estructura hueca. Los tucanes viven en selvas tropicales y son frugívoros, aunque también comen insectos y pequeños reptiles. Son aves muy sociables y suelen formar grupos, usando su pico para comunicarse entre ellos. Su plumaje vibrante y sus colores lo hacen un espectáculo visual en la naturaleza.'
    },

  ])
</script>

<template>
  <Navbar />
    <main>
      <h1>Bienvenido a mi sitio</h1>
    </main>
    <Cards 
      class="card"
      v-for="card in cards" 
      :key="card.title" 
      :image="card.image"
      :title="card.title"
      :description="card.description"
      :content="card.content"
    />
  <Footer />
</template>

<style scoped>

</style>
