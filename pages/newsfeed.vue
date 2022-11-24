<template>
  <NuxtLayout>
    <div class="flex flex-wrap justify-center">
      <div
        class="w-full lg:w-5/6 p-2 flex flex-col justify-center items-center"
      >
        <p
          class="text-xl p-2 bg-yellow-500 text-white rounded-sm my-4 w-full text-center shadow-lg mx-2"
        >
          NEWSFEED
        </p>
      </div>
    </div>
    <div class="flex flex-col items-center mb-5 p-2 space-y-4">
      <div
        v-for="newsitem in data.newsfeeds"
        :key="newsitem.id"
        class="lg:w-full flex justify-center"
      >
        <CardNewsFeed
          :title="newsitem.title"
          :imageProfile="newsitem.imageProfile"
          :content="newsitem.description"
          :constributor="newsitem.author"
          :published="newsitem.createdat"
        />
      </div>
    </div>
  </NuxtLayout>
  <DivFooter />
</template>

<script setup>
const { data } = await useFetch("/api/newsfeed");
</script>
