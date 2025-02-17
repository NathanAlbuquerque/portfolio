<script setup>
import TheNav from './components/TheNav.vue'
import SkillItem from './components/SkillItem.vue'

const skills = ['HTML', 'CSS', 'TailwindCSS', 'JavaScript', 'NodeJS', 'TypeScript', 'ReactJS', 'NextJS', 'VueJS', 'PHP', 'Laravel']
</script>

<template>
  <header class="flex justify-center my-5">
    <div class="container fixed py-2.5 px-4.5 flex justify-between items-center rounded-4xl bg-slate-200/20 border border-slate-200/30 backdrop-blur-sm shadow-md">
      <img src="@/assets/perfil-nathan-albuquerque.png" class="rounded-full" width="40" height="40" alt="Perfil Nathan Albuquerque">
      <TheNav/>
    </div>
  </header>
  <div class="h-18"></div>
  <main class="py-12 flex justify-center">
    <div class="container" id="skills">
      <h1 class="text-6xl font-black">Nathan Reinaldo de Albuquerque</h1>
      <p class="mt-6 text-4xl font-bold text-gray-800">Skills</p>
      <div class="mt-4 px-4 grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-5 gap-4 place-items-center">
        <SkillItem v-for="skill in skills" :key="skill" :titulo="skill"/>
      </div>
    </div>
  </main>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
</template>
