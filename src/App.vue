<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheNav from './components/TheNav.vue'
</script>

<template>
  <header class="flex justify-center">
    <div class="container py-2.5 px-4.5 flex justify-between items-center rounded-4xl bg-gray-300/20 border border-gray-200/30 backdrop-blur-sm shadow-md">
      <img src="@/assets/perfil-nathan-albuquerque.png" class="rounded-full" width="40" height="40" alt="Perfil Nathan Albuquerque">
      <TheNav/>
    </div>
  </header>

</template>
