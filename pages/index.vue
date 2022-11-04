<template>
  <NuxtLayout>
    <div class="flex flex-wrap justify-center">
      <div
        class="w-full md:w-1/2 p-2 flex flex-col justify-center items-center"
      >
        <p
          class="
            text-xl
            py-2
            px-1
            bg-yellow-500
            text-white
            rounded-sm
            my-4
            w-full
            text-center
            shadow-lg
            mx-2
          "
        >
          Cerita Usaha
        </p>
      </div>
    </div>
    <div class="flex flex-wrap justify-center">
      <div
        class="
          w-full
          md:w-1/2
          lg:w-5/6
          p-2
          flex flex-col
          lg:grid lg:grid-cols-3
          gap-4
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
          <!-- component card -->
          <card-cerita
            :imageProfile="item.imageProfile"
            :nameProfile="item.nameProfile"
            :image="item.image"
            :judul="item.title"
            :isi="item.description"
          />
          <!-- end component card -->
        </div>
      </div>
    </div>
  </NuxtLayout>
</template>
<script>
import CardCerita from "~~/components/CardCerita.vue";
// card product
export default {
  components: { CardCerita },
  //   data to cardCerita

  data() {
    return {
      data: [
        {
          id: 1,
          imageProfile: "https://picsum.photos/seed/picsum/200/300",
          nameProfile: "Nama Profile",
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
      ],
    };
  },
};
</script>
