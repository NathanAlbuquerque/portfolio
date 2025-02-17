<script setup>
import TheNav from './components/TheNav.vue'
import SkillItem from './components/SkillItem.vue'

const skills = ['HTML', 'CSS', 'TailwindCSS', 'JavaScript', 'NodeJS', 'TypeScript', 'ReactJS', 'NextJS', 'VueJS', 'PHP', 'Laravel']

const projetosProfisionais = [
  {
    url: 'https://www.lojazacks.com.br/',
    imagem: 'src/assets/imagens/projeto-profissional-loja-zacks.png',
    nome: 'Site Institucional + e-commerce de venda de instrumentos',
    servico: 'Manutenção e suporte',
  },
  {
    url: 'https://campeonatovoolivre.com.br/',
    imagem: 'src/assets/imagens/projeto-profissional-11-campeonato-de-voo-livre.png',
    nome: 'Landing page para divulgação de evento',
    servico: 'Projeto completo',
  },
  {
    url: 'https://gruponovaluz.com.br/',
    imagem: 'src/assets/imagens/projeto-profissional-eccommerce-nova-luz.png',
    nome: 'Site Institucional + e-commerce de venda de materiais elétricos',
    servico: 'Projeto completo (menos API de pagamentos)',
  },
  {
    url: 'https://racoesaquario.com.br/',
    imagem: 'src/assets/imagens/projeto-profissional-racoes-aquario.png',
    nome: 'Site institucional',
    servico: 'Manutenção e suporte',
  },
  {
    url: 'https://oculoscarpediem.com.br/',
    imagem: 'src/assets/imagens/projeto-profissional-oculos-carpe-diem.png',
    nome: 'Site institucional de marca de óculos',
    servico: 'Atualização de manutenção',
  },
  {
    url: 'https://clinicaprovir.com/',
    imagem: 'src/assets/imagens/projeto-profissional-clinica-provir.png',
    nome: 'Site institucional de clinica admissional',
    servico: 'Projeto completo',
  },
]
// https://kellysemijoias.nuvemshop.com.br/

</script>

<template>
  <header class="flex justify-center my-5">
    <div class="container fixed py-2.5 px-4.5 flex justify-between items-center rounded-4xl bg-slate-200/20 border border-slate-200/30 backdrop-blur-sm shadow-md">
      <img src="@/assets/imagens/perfil-nathan-albuquerque.png" class="rounded-full" width="40" height="40" alt="Perfil Nathan Albuquerque">
      <TheNav/>
    </div>
  </header>

  <div class="h-18"></div>

  <main class="py-12 flex flex-col items-center gap-20">

    <div class="container" id="skills">
      <h1 class="text-6xl font-black">Nathan Reinaldo de Albuquerque</h1>
      <p class="mt-8 text-4xl font-bold text-gray-800">Skills</p>
      <div class="mt-6 px-4 grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-5 gap-4 place-items-center">
        <SkillItem v-for="skill in skills" :key="skill" :titulo="skill"/>
      </div>
    </div>

    <div class="container bg-radial from-slate-300 to-white to-60% h-px w-full"></div>

    <div class="container" id="projetos-profissionais">
      <p class="text-4xl font-bold text-gray-800">Projetos Profisionais</p>
      <div class="mt-6 px-4 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 place-items-center content-center">

        <div v-for="projeto in projetosProfisionais" :key="projeto.url" class="w-full h-full max-h-max rounded-2xl bg-slate-100 border border-slate-300 shadow-md text-lg text-center hover:scale-105 transition cursor-default overflow-hidden">
          <img class="border-b border-b-slate-300" :src="projeto.imagem" alt="">
          <div class="pt-5 px-4 pb-8 text-left">
            <h3 class="text-gray-900 text-lg">{{ projeto.nome }}</h3>
            <p class="text-gray-800 text-sm">{{ projeto.servico }}</p>
          </div>
        </div>

      </div>
    </div>

    <div class="container bg-radial from-slate-300 to-white to-60% h-px w-full"></div>

    <div class="container" id="sobre-mim">
      <p class="text-4xl font-bold text-gray-800">Sobre mim</p>
      <p class="mt-4 text-xl text-gray-800">Jovem desenrolado, responsável e estudioso, tenho alguns projetos no ar, mas busco uma oportunidade remota. Se interessou pelos meus serviços? Me mande um e-mail.</p>
      <div class="flex space-x-6 mt-6">
        <a href="https://github.com/NathanAlbuquerque" target="_blank" rel="noopener noreferrer" class="w-14 h-14 grid place-content-center rounded-full bg-cyan-300 hover:scale-105 transition"><img src="@/assets/imagens/github.svg" width="38" height="38" alt=""></a>
        <a href="https://www.linkedin.com/in/nathan-albuquerque/" target="_blank" rel="noopener noreferrer" class="w-14 h-14 grid place-content-center rounded-full bg-cyan-300 hover:scale-105 transition"><img src="@/assets/imagens/linkedin.svg" width="28" height="28" alt=""></a>
      </div>
    </div>

  </main>
</template>
