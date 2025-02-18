<script setup>
import { ref } from 'vue';

const links = [
    { url: '#skills', titulo: 'Skills' },
    { url: '#projetos-profissionais', titulo: 'Profissional' },
    // { url: '#', titulo: 'Pessoal' },
    { url: '#sobre-mim', titulo: 'Sobre mim' },
]
const tema = ref(localStorage.theme ? localStorage.theme : 'light')
const mudarTema = (cor) => {
    // localStorage.removeItem("theme");
    localStorage.theme = localStorage.theme == 'dark' ? 'light' : 'dark'
    tema.value = localStorage.theme
    document.documentElement.classList.toggle('dark')
}
document.documentElement.classList.toggle("dark", localStorage.theme === "dark" || (!("theme" in localStorage) && window.matchMedia("(prefers-color-scheme: dark)").matches),);
</script>

<template>
    <nav class="px-9 rounded-full space-x-6 sm:space-x-10 font-medium tracking-wide">
        <a v-for="link in links" :key="link.titulo" :href="link.url" class="text-sm sm:text-base hover:underline dark:text-white">{{ link.titulo }}</a>
        <img @click="mudarTema('light')" :src="`src/assets/imagens/${tema}-mode.svg`" class="inline cursor-pointer hover:animate-pulse" width="20" height="20" alt="">
    </nav>
</template>
