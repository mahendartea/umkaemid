<template>
  <!-- card tailwind with props -->

  <div class="flex items-center justify-start m-2 p-4">
    <img
      class="w-8 h-8 rounded-full object-cover object-center"
      :src="imageProfile"
    />
    <p class="py-2 mx-2">{{ nameProfile }}</p>
  </div>
  <div class="w-full h-48 overflow-hidden">
    <img
      class="w-full h-full object-cover object-center"
      :src="image"
      alt="card"
    />
  </div>
  <div class="p-4">
    <h2 class="text-lg font-semibold text-gray-800 mb-2">Cerita Usaha</h2>
    <p
      class="
        text-gray-700 text-sm
        mb-2
        first-letter:text-7xl
        first-letter:font-bold
        first-letter:text-slate-900
        first-letter:mr-3
        first-letter:float-left
      "
    >
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam
      voluptates, quod, quia, voluptate quae voluptatem quibusdam voluptatibus
      <span class="font-semibold block hover:text-yellow-700 cursor-pointer"
        >Selengkapnya..</span
      >
    </p>
  </div>
  <div class="px-4">
    <!-- product description -->
    <div class="flex item-center justify-between my-5">
      <div class="flex item-center space-x-4">
        <div class="flex item-center">
          <font-awesome-icon :icon="['fas', 'tag']" class="text-gray-500" />
        </div>
        <p class="text-gray-500 text-sm">Product and description</p>
      </div>
      <div class="flex item-center space-x-4">
        <div class="flex item-center">
          <font-awesome-icon
            :icon="['fas', 'map-marker-alt']"
            class="text-gray-500"
          />
          <!-- <font-awesome-icon icon="far-regular fa-map-marker-alt" class="text-gray-500" /> -->
        </div>
        <p class="text-gray-500 text-sm">Lokasi</p>
      </div>
    </div>
  </div>
  <div class="flex p-2 border-t border-gray-200 justify-between">
    <div class="flex items-center justify-between my-2 w-full px-2">
      <!-- icon media social like comment share with fontawesome -->
      <div class="flex item-center space-x-4">
        <div
          class="
            flex
            items-center
            justify-center
            w-8
            h-8
            rounded-full
            bg-gray-100
          "
        >
          <font-awesome-icon
            :icon="['fas', 'thumbs-up']"
            class="text-red-500"
          />
          <!-- <font-awesome-icon icon="fas-regular fa-thumbs-up" class="text-red-500" /> -->
        </div>
        <div
          class="
            flex
            items-center
            justify-center
            w-8
            h-8
            rounded-full
            bg-gray-100
          "
        >
          <font-awesome-icon
            :icon="['fas', 'comments']"
            class="text-gray-500"
          />
          <!-- <font-awesome-icon icon="fas-regular fa-comment" class="text-gray-500" /> -->
        </div>
        <div
          class="
            flex
            items-center
            justify-center
            w-8
            h-8
            rounded-full
            bg-gray-100
          "
        >
          <font-awesome-icon
            :icon="['fas', 'share-square']"
            class="text-gray-500"
          />
          <!-- <font-awesome-icon icon="fas-regular fa-share-square" class="text-gray-500" /> -->
        </div>
      </div>
      <div class="flex item-center justify-between space-x-4">
        <!-- human time and info -->
        <div class="flex item-center space-x-4">
          <div class="flex item-center">
            <font-awesome-icon :icon="['fas', 'clock']" class="text-gray-500" />
            <!-- <font-awesome-icon icon="fas-regular fa-clock" class="text-gray-500" /> -->
          </div>
          <p class="text-gray-500 text-sm">1 jam yang lalu</p>
        </div>
      </div>
    </div>
  </div>
  <div class="flex item-center justify-center my-5 px-2 w-full">
    <div class="flex item-center justify-between space-x-4">
      <div class="flex item-center">
        <img
          class="w-8 h-8 rounded-full object-cover object-center"
          :src="image"
        />
      </div>
      <div class="flex item-center">
        <input
          type="text"
          class="w-full h-8 rounded-full bg-gray-100 text-gray-500 px-2"
          placeholder="Tulis komentar..."
        />
      </div>
      <div>
        <font-awesome-icon
          :icon="['fas', 'paper-plane']"
          class="text-gray-500"
        />
        <!-- <font-awesome-icon icon="paper-plane" class="icon alt" /> -->
      </div>
    </div>
  </div>
</template>
<script>
// props
export default {
  //  props card
  props: {
    imageProfile: {
      type: String,
      default: "https://picsum.photos/seed/picsum/200/300",
    },
    nameProfile: {
      type: String,
      default: "Nama Profile",
    },
    image: {
      type: String,
      default: "https://picsum.photos/200/300",
    },
    judul: {
      type: String,
      default: "Judul Cerita",
    },
    isi: {
      type: String,
      default: "Isi Cerita",
    },
  },
};
</script>
