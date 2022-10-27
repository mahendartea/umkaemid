<template>
  <div class="bg-[#e6e6e6] fixed top-0 w-full z-50">
    <!-- navbar fixed with tailwindcss -->

    <nav class="px-5 m-auto flex items-center py-2 justify-between h-14">
      <div class="md:flex md:justify-between items-center md:w-1/3 w-1/2">
        <div class="md:flex justify-start items-center">
          <NuxtLink to="/">
            <img src="/img/uemkaem.png" alt="logo" class="md:h-5 md:mx-5 h-6" />
          </NuxtLink>
          <div class="hidden lg:flex">
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
        <ul
          class="
            md:flex md:justify-between
            items-center
            m-auto
            md:space-x-4
            hidden
          "
        >
          <NuxtLink :to="l.link" v-for="l in navbar" :key="l.id">
            <li
              class="
                flex
                text-slate-600 text-sm
                hover:text-[#ebb22b]
                focus:outline-none focus:text-[#ebb22b]
                font-semibold
                py-2
                rounded
                transition
                duration-300
                ease-in-out
              "
              :class="{ 'text-[#ebb22b]': $route.path === l.link }"
            >
              <img
                :alt="l.alt"
                :src="l.image"
                class="mx-1 hidden lg:block"
                height="23"
                width="23"
                :key="l.image"
              />
              <p class="lg:w-32 text-sm">{{ l.navbarName }}</p>
            </li>
          </NuxtLink>
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
          <NuxtLink to="/register">
            <a
              href="#"
              class="
                px-3
                py-1
                rounded-md
                bg-[#ebb22b]
                hover:bg-yellow-300
                text-white
                transition
                duration-300
                ease-in-out
              "
              >Daftar
            </a>
          </NuxtLink>
          <NuxtLink to="/login">
            <a href="#" class="px-2 text-slate-600 hover:text-slate-700 text-sm"
              >Login</a
            >
          </NuxtLink>
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
            py-2
            rounded-b
          "
        >
          <div class="mb-2" v-for="ml in navbar" :key="ml.id">
            <NuxtLink
              class="px-2 text-slate-600 hover:text-slate-700"
              :to="ml.link"
              >{{ ml.navbarName }}</NuxtLink
            >
          </div>
          <NuxtLink
            to="/register"
            class="w-2/3 rounded-md bg-[#ebb22b] text-white py-1"
          >
            <a href="#" class="px-2 hover:text-slate-700">Daftar </a>
          </NuxtLink>
          <NuxtLink to="/login">
            <a href="#" class="px-2 text-slate-600 hover:text-slate-700"
              >Login</a
            >
          </NuxtLink>
        </div>
      </div>
    </nav>
  </div>
</template>
<script>
export default {
  data() {
    return {
      navbar: [
        {
          navbarName: "Cerita Usaha",
          image: "/img/beranda-act.png",
          alt: "Cerita Usaha",
          link: "/",
        },
        {
          navbarName: "Newsfeed",
          image: "/img/newsfeed-non.png",
          alt: "newsfeed",
          link: "/newsfeed",
        },
        {
          navbarName: "Marketplace",
          image: "/img/marketplace-non.png",
          alt: "marketplace",
          link: "/marketplace",
        },
      ],
      showMenu: false,
    };
  },
};
</script>
