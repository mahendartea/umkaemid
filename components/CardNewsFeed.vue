<template>
  <div
    v-for="newsitem in data.newsfeeds"
    :key="newsitem.id"
    class="lg:w-full flex justify-center"
  >
    <div
      class="w-full lg:w-5/6 px-10 py-5 flex items-center justify-center border border-slate-300 shadow-lg rounded-lg"
    >
      <div class="w-1/5 rounded-lg overflow-auto">
        <img
          :src="newsitem.imageProfile"
          alt="profil"
          width="200"
          height="200"
        />
      </div>
      <div
        class="w-5/6 flex flex-col items-start justify-start content-start px-5 h-full"
      >
        <h1 class="text-2xl fond-bold mb-8">
          {{ newsitem.title }}
        </h1>
        <hr />
        <p class="text-sm my-3">
          {{ newsitem.description }}
        </p>
        <div class="w-full flex items-center justify-between">
          <p class="text-md">{{ newsitem.author }}</p>
          <p class="text-xs text-slate-400">{{ newsitem.createdat }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
const { data } = await useAsyncData("cerita", () => $fetch("/api/newsfeed"));
</script>
