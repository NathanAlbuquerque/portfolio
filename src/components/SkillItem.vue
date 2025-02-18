<script setup>
defineProps({
  titulo: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <span class="w-full max-w-60 py-3 rounded-full bg-slate-100 border border-slate-300 dark:border-slate-600 dark:bg-gray-700 dark:hover:bg-gray-600 shadow-md dark:text-white text-lg text-center hover:scale-[105%_110%] transition cursor-default">{{ titulo }}</span>
</template>