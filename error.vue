<template>
  <div
    class="flex flex-col mx-auto items-center mt-48 bg-[#ebb22b] py-10 text-white gap-y-7"
  >
    <h3 class="text-7xl font-bold">{{ error.statusCode }}</h3>
    <p class="text-6xl font-bold">OOPS - {{ error.message }}</p>
    <button @click="handleError" class="btn max-w-sm">Clear Page</button>
  </div>
</template>

<script setup>
const props = defineProps({
  error: Object,
});

const handleError = () => clearError({ redirect: "/" });
</script>
