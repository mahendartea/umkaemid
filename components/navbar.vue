<template>
  <!-- navbar tailwind responsize example -->

  <div class="bg-[#e6e6e6]">
    <nav class="px-5 m-auto flex items-center py-2 justify-between h-14">
      <div class="md:flex md:justify-between items-center md:w-1/3 w-1/2">
        <div class="md:flex justify-start items-center">
          <img
            src="~/assets/img/uemkaem.png"
            alt="logo"
            class="md:h-5 md:mx-5 h-6"
          />
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
          <li class="px-2 flex text-slate-600 hover:text-slate-700 text-sm">
            <img
              class="mx-1"
              src="~/assets/img/beranda-act.png"
              alt="beranda"
              width="23"
              height="23"
            /><a href="#"> Cari Usaha</a>
          </li>
          <li class="px-2 flex text-slate-600 hover:text-slate-700 text-sm">
            <img
              class="mx-1"
              src="~/assets/img/newsfeed-non.png"
              alt="beranda"
              width="23"
              height="23"
            /><a href="#">NewFeed</a>
          </li>
          <li class="px-2 flex text-slate-600 hover:text-slate-700 text-sm">
            <img
              class="mx-1"
              src="~/assets/img/marketplace-non.png"
              alt="beranda"
              width="23"
              height="23"
            /><a href="#">Merketpreneur</a>
          </li>
        </ul>
      </div>
      <div class="md:w-1/3 md:flex md:justify-end text-end">
        <!-- humberger menu tailwind -->
        <button
          class="
            md:hidden
            border border-slate-400/20
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
          <a href="#" class="px-2 text-slate-600 hover:text-slate-700">Masuk</a>
        </div>
      </div>
    </nav>
  </div>
</template>
