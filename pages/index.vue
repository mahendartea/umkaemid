<template>
  <NuxtLayout>
    <div class="flex flex-wrap justify-center">
      <div
        class="w-full md:w-5/6 p-2 flex flex-col justify-center items-center"
      >
        <p
          class="text-xl p-2 bg-yellow-500 text-white rounded-sm my-4 w-full text-center shadow-lg mx-2"
        >
          CERITA USAHA
        </p>
      </div>
    </div>
    <div class="flex flex-wrap justify-center mb-5">
      <div
        class="w-full md:w-1/2 lg:w-5/6 p-2 flex flex-col lg:grid lg:grid-cols-3 gap-4 justify-center items-center"
      >
        <div
          v-for="item in data.cerita"
          :key="item.id"
          class="my-2 w-full h-full bg-white shadow-lg rounded-lg overflow-hidden flex flex-col justify-between border border-gray-200 p-0"
        >
          <!-- component card -->
          <card-cerita
            :imageProfile="item.imageProfile"
            :nameProfile="item.nameProfile"
            :image="item.image"
            :judul="item.title"
            :like="item.counLike"
            :comments="item.countComment"
            :productDesc="item.description"
          />
          <!-- end component card -->
        </div>
      </div>
    </div>
    <Paging />
  </NuxtLayout>
  <DivFooter />
</template>

<script setup>
const { data } = await useFetch("/api/cerita");
</script>
