<template>
  <!-- navbar tailwind responsize example -->

  <div class="bg-[#e6e6e6]">
    <nav class="px-5 m-auto flex items-center py-2 justify-between h-14">
      <div class="md:flex md:justify-between items-center md:w-1/3 w-1/2">
        <div class="md:flex justify-start items-center">
          <img src="/img/uemkaem.png" alt="logo" class="md:h-5 md:mx-5 h-6" />
          <div class="hidden md:flex">
            <input
              type="text"
              placeholder="Pencarian Anda"
              class="
                w-44
                rounded-l
                md:h-9
                px-5
                py-1
                focus:outline-none
                placeholder:text-slate-500
                placeholder:font-light
                placeholder:text-sm
                border border-slate-300 border-r-0
              "
            />
            <button
              class="
                bg-[#ebb22b]
                hover:bg-[#ffe924]
                border-[#ffe817]
                py-1
                px-3
                rounded-r
                h-9
              "
            >
              <font-awesome-icon icon="fas fa-search" class="text-white" />
            </button>
          </div>
        </div>
      </div>
      <div class="text-center md:w-1/3">
        <ul class="lg:flex lg:justify-between items-center m-auto hidden">
          <li
            v-for="l in navbar"
            :key="l.id"
            class="px-2 flex text-slate-600 hover:text-slate-700 text-sm"
          >
            <img
              :alt="l.alt"
              :src="l.image"
              class="mx-1"
              height="23"
              width="23"
              :key="l.image"
            /><a href="#"> {{ l.navbarName }}</a>
          </li>
        </ul>
      </div>
      <div class="md:w-1/3 md:flex md:justify-end text-end">
        <!-- humberger menu tailwind -->
        <button
          @click="showMenu = !showMenu"
          class="
            md:hidden
            border border-slate-600/20
            px-4
            py-1
            rounded
            hover:bg-slate-300
          "
        >
          <font-awesome-icon icon="fa-solid fa-bars" class="text-slate-500" />
        </button>
        <div class="hidden md:flex">
          <a href="#" class="px-2 text-slate-600 hover:text-slate-700"
            >Daftar
          </a>
          <a href="#" class="px-2 text-slate-600 hover:text-slate-700">Login</a>
        </div>
        <!-- menu mobile version tailwind -->
        <div
          v-if="showMenu"
          class="
            md:hidden
            absolute
            top-14
            right-0
            w-full
            bg-[#e6e6e6]
            flex flex-col
            items-center
            text-center
            py-2rounded-b
          "
        >
          <div class="mb-2">
            <a href="#" class="px-2 text-slate-600 hover:text-slate-700"
              >Beranda</a
            >
            <a href="#" class="px-2 text-slate-600 hover:text-slate-700"
              >Newsfeed</a
            >
            <a href="#" class="px-2 text-slate-600 hover:text-slate-700"
              >MarketPlace</a
            >
          </div>
          <a
            href="#"
            class="px-2 border border-t-2 text-slate-600 hover:text-slate-700"
            >Daftar</a
          >
          <a href="#" class="px-2 text-slate-600 hover:text-slate-700">Login</a>
        </div>
      </div>
    </nav>
  </div>
</template>
<script>
export default {
  //image looping v-for
  data() {
    return {
      navbar: [
        {
          navbarName: "Beranda",
          image: "/img/beranda-act.png",
          alt: "beranda",
        },
        {
          navbarName: "newsfeed",
          image: "/img/newsfeed-non.png",
          alt: "newsfeed",
        },
        {
          navbarName: "marketplace",
          image: "/img/marketplace-non.png",
          alt: "marketplace",
        },
      ],
      showMenu: false,
    };
  },
};
</script>
