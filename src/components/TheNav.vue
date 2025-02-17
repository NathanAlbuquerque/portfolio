<script setup>
const links = [
    { url: '#skills', titulo: 'Skills' },
    { url: '#projetos-profissionais', titulo: 'Profissional' },
    // { url: '#', titulo: 'Pessoal' },
    { url: '#sobre-mim', titulo: 'Sobre mim' },
]
</script>

<template>
    <nav class="px-9 rounded-full space-x-10 font-medium tracking-wide">
        <a v-for="link in links" :key="link.titulo" :href="link.url" class="hover:underline">{{ link.titulo }}</a>
    </nav>
</template>
