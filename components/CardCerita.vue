<template>
  <!-- card tailwind with props -->
  <div class="flex items-center justify-start m-2 p-2">
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
  <div class="px-4 my-2">
    <p class="text-md font-semibold text-gray-800">{{ judul }}</p>
  </div>
  <div class="px-4">
    <!-- product description -->
    <div class="flex item-center justify-between my-2">
      <div class="flex item-center space-x-4">
        <div class="flex item-center">
          <Icon class="text-gray-500" name="mdi:tag" />
        </div>
        <p class="text-gray-500 text-sm pr-5">{{ productDesc }}</p>
      </div>
      <div class="flex item-center space-x-4">
        <div class="flex item-center">
          <Icon name="material-symbols:location-on" class="text-gray-500" />
        </div>
        <p class="text-gray-500 text-sm">Jakarta</p>
      </div>
    </div>
  </div>
  <div class="flex item-center p-2 border-t border-gray-200 justify-between">
    <div class="flex items-center justify-between my-2 w-full px-4">
      <div class="flex item-center gap-4">
        <div class="flex items-center justify-center w-8 h-8 rounded-full">
          <div class="flex gap-1 items-center">
            <Icon name="bi:hand-thumbs-up-fill" class="text-red-600" />
          </div>
          <span class="text-sm mx-1 text-gray-500">{{ like }}</span>
        </div>
        <div class="flex items-center justify-center w-8 h-8 rounded-full">
          <div class="mx-1">
            <Icon name="fa6-regular:comments" />
          </div>
          <span class="text-sm mx-1 text-gray-500">{{ comments }}</span>
        </div>
        <div class="flex items-center justify-center w-8 h-8 rounded-full">
          <Icon name="ri:share-forward-2-fill" />
        </div>
      </div>
      <div class="flex item-center justify-between space-x-4">
        <!-- human time and info -->
        <div class="flex item-center space-x-4">
          <div class="flex item-center">
            <Icon name="mdi:clock-outline" />
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
        <Icon
          name="ri:send-plane-fill"
          width="28"
          height="28"
          class="text-gray-500"
        />
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
    like: {
      type: Number,
      default: 0,
    },
    comments: {
      type: Number,
      default: 0,
    },
    productDesc: {
      type: String,
      default: "Product Desc",
    },
  },
};
</script>
