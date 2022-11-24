<template>
  <div
    class="w-full lg:w-5/6 px-10 py-5 flex items-center justify-center border border-slate-300 shadow-lg rounded-lg"
  >
    <div class="w-1/5 rounded-lg overflow-auto">
      <img :src="imageProfile" alt="profil" width="200" height="200" />
    </div>
    <div
      class="w-5/6 flex flex-col items-start justify-start content-start px-5 h-full"
    >
      <h1 class="text-2xl fond-bold mb-8">
        {{ title }}
      </h1>
      <hr />
      <p class="text-sm my-3">
        {{ content }}
      </p>
      <div class="w-full flex items-center justify-between">
        <p class="text-md">{{ contributor }}</p>
        <p class="text-xs text-slate-400">{{ published }}</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    imageProfile: {
      type: String,
      default: "https://uemkaem.id/images/logo/thumbnail/1661157242.png",
    },
    title: {
      type: String,
      default: "https://uemkaem.id/images/logo/thumbnail/1661157242.png",
    },
    content: {
      type: String,
      default: "",
    },
    contributor: {
      type: String,
      default: "UEMKAEMID",
    },
    published: {
      type: String,
      default: "Sabtu, 20-12-2022",
    },
  },
};
</script>
