<template>
  <NuxtLayout>
    <div class="p-10 item-center h-full bg-[#F8FAFC]">
      <div class="md:flex md:m-auto md:container">
        <div class="hidden md:flex items-center md:w-1/2 md:mr-20 md:m-auto">
          <img
            src="/img/uemkaem-logo-horizontal.png"
            alt="logo"
            class="md:mx-5 md:max-w-20"
          />
        </div>
        <div class="space-y-5 md:w-1/2">
          <h1 class="py-3 font-bold font-sans text-slate-700">Login</h1>
          <div v-for="form in formLogin" :key="form.id">
            <div
              class="flex h-10 md:max-w-md border border-slate-500 rounded-md"
            >
              <label
                :for="form.forLabel"
                class="
                  flex
                  items-center
                  px-3
                  py-2
                  bg-slate-200
                  rounded-l-md
                  border-r border-slate-500
                "
              >
                <font-awesome-icon :icon="form.icon" class="text-slate-700" />
              </label>
              <input
                :name="form.name"
                :placeholder="form.placeholder"
                :type="form.type"
                class="w-full rounded-r-md p-1"
              />
            </div>
          </div>

          <div class="flex items-start">
            <input
              type="checkbox"
              name="remember"
              id="remember"
              class="
                h-4
                w-4
                text-blue-600
                focus:ring-blue-500
                border-gray-300
                rounded
                mx-2
              "
            />
            <label for="remember" class="block text-sm text-gray-900">
              Simpan akun saya
            </label>
          </div>

          <div class="px-10 text-center leading-loose max-w-md">
            <Button>Login</Button>
          </div>
        </div>
      </div>
    </div>
  </NuxtLayout>
</template>

<script>
export default {
  data() {
    return {
      formLogin: [
        {
          forLabel: "email",
          icon: "fas-solid fa-envelope",
          name: "email",
          placeholder: "Masukan email anda..",
          type: "text",
        },
        {
          forLabel: "password",
          icon: "fas-solid fa-lock",
          name: "password",
          placeholder: "Masukan password anda..",
          type: "password",
        },
      ],
    };
  },
};
</script>
