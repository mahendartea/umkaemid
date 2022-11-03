<template>
  <NuxtLayout>
    <div class="flex item-center justify-center mt-20">
      <p
        class="
          text-xl
          py-2
          px-1
          bg-yellow-500
          text-white
          rounded-sm
          my-5
          w-full
          text-center
          shadow-lg
          mx-2
        "
      >
        Cerita Usaha
      </p>
    </div>
    <!-- card mobile with tailwindcss -->

    <!-- card media social tailwind-->
    <div class="flex flex-wrap justify-center">
      <div
        class="
          w-full
          md:w-1/2
          lg:w-1/3
          xl:w-1/4
          p-2
          flex flex-col
          justify-center
          items-center
        "
      >
        <div
          v-for="item in data"
          :key="item.id"
          class="
            my-2
            w-full
            h-full
            bg-white
            shadow-lg
            rounded-lg
            overflow-hidden
            flex flex-col
            justify-between
            border border-gray-200
            p-0
          "
        >
          <div class="flex items-center justify-start m-2 p-4">
            <img
              class="w-8 h-8 rounded-full object-cover object-center"
              :src="item.image"
            />
            <p class="py-2 mx-2">Akun Product</p>
          </div>
          <div class="w-full h-48 overflow-hidden">
            <img
              class="w-full h-full object-cover object-center"
              :src="item.image"
              alt="card"
            />
          </div>
          <div class="p-4">
            <h2 class="text-lg font-semibold text-gray-800">Cerita Usaha</h2>
            <p class="text-gray-700 text-sm mb-2">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam
              voluptates, quod, quia, voluptate quae voluptatem quibusdam
              voluptatibus quidem quos quas.
            </p>
          </div>
          <div class="px-4">
            <!-- product description -->
            <div class="flex item-center justify-between my-5">
              <div class="flex item-center space-x-4">
                <div class="flex item-center">
                  <font-awesome-icon
                    icon="far-regular fa-tag"
                    class="text-gray-500"
                  />
                </div>
                <p class="text-gray-500 text-sm">Product and description</p>
              </div>
              <div class="flex item-center space-x-4">
                <div class="flex item-center">
                  <font-awesome-icon
                    icon="far-regular fa-map-marker-alt"
                    class="text-gray-500"
                  />
                </div>
                <p class="text-gray-500 text-sm">Lokasi</p>
              </div>
            </div>
          </div>
          <div class="flex p-2 border-t border-gray-200 justify-between">
            <div class="flex items-center justify-between my-2 w-full">
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
                    icon="far-regular fa-thumbs-up"
                    class="text-red-500"
                  />
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
                    icon="far-regular fa-comment"
                    class="text-gray-500"
                  />
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
                    icon="far-regular fa-share-square"
                    class="text-gray-500"
                  />
                </div>
              </div>
              <div class="flex item-center justify-between space-x-4">
                <!-- human time and info -->
                <div class="flex item-center space-x-4">
                  <div class="flex item-center">
                    <font-awesome-icon
                      icon="far-regular fa-clock"
                      class="text-gray-500"
                    />
                  </div>
                  <p class="text-gray-500 text-sm">1 jam yang lalu</p>
                </div>
              </div>
            </div>
          </div>
          <div class="flex item-center justify-center my-2 px-2 w-full">
            <div class="flex item-center justify-between space-x-4">
              <div class="flex item-center">
                <img
                  class="w-8 h-8 rounded-full object-cover object-center"
                  :src="item.image"
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
                <font-awesome-icon icon="fa-solid fa-paper-plane" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </NuxtLayout>
</template>
<script>
// card product
export default {
  data() {
    return {
      data: [
        {
          id: 1,
          title: "Cerita Usaha 1",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image: "https://picsum.photos/200/300",
        },
        {
          id: 2,
          title: "Cerita Usaha 2",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image: "https://random.imagecdn.app/500/150",
        },
        {
          id: 3,
          title: "Cerita Usaha 3",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image: "https://picsum.photos/200/300",
        },
        {
          id: 4,
          title: "Cerita Usaha 4",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image: "https://picsum.photos/200/300",
        },
        {
          id: 5,
          title: "Cerita Usaha 5",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image: "https://picsum.photos/200/300",
        },
        {
          id: 6,
          title: "Cerita Usaha 6",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image: "https://picsum.photos/200/300",
        },
        {
          id: 7,
          title: "Cerita Usaha 7",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image: "https://picsum.photos/200/300",
        },
        {
          id: 8,
          title: "Cerita Usaha 8",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image: "https://picsum.photos/200/300",
        },
        {
          id: 9,
          title: "Cerita Usaha 9",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image: "https://picsum.photos/200/300",
        },
        {
          id: 10,
          title: "Cerita Usaha 10",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image: "https://picsum.photos/200",
        },
      ],
    };
  },
};
</script>
