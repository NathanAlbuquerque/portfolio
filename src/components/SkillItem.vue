<script setup>
defineProps({
  titulo: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <span class="w-full max-w-60 py-3 rounded-full bg-slate-100 border border-slate-300 shadow-md text-lg text-center hover:scale-105 transition cursor-default">{{ titulo }}</span>
</template>