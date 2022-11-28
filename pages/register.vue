<template>
  <NuxtLayout>
    <Head>
      <Title>Uemkaem.id | Register</Title>
      <Meta name="description" content="Home website uemkaemid Indonesia" />
    </Head>
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
          <h1 class="py-3 font-bold font-sans text-slate-700">
            Registerasi Akun
          </h1>
          <div v-for="form in formRegister" :key="form.id">
            <div
              class="flex h-10 md:max-w-md border border-slate-500 rounded-md"
            >
              <label
                :for="form.forLabel"
                class="flex items-center px-3 py-2 bg-slate-200 rounded-l-md border-r border-slate-500"
              >
                <Icon :name="form.icon" class="text-slate-700" />
              </label>
              <input
                :name="form.name"
                :placeholder="form.placeholder"
                :type="form.type"
                class="w-full rounded-r-md p-1"
              />
            </div>
          </div>

          <div class="px-10 py-3 text-center leading-loose max-w-md">
            <p class="text-xs text-slate-800 font-sans">
              Dengan mengklik Setuju & Daftar, Anda menyetujui
              <span class="text-blue-700">Syarat & Ketentuan</span> serta
              <span class="text-blue-700">Kebijakan Privasi</span> dari
              uemkaem.id
            </p>
            <Button>Setuju & Daftar</Button>
          </div>
        </div>
      </div>
    </div>
    <DivFooter />
  </NuxtLayout>
</template>

<script>
export default {
  data() {
    return {
      formRegister: [
        {
          forLabel: "username",
          icon: "mdi:user-circle-outline",
          name: "username",
          placeholder: "Masukan username anda..",
          type: "text",
        },
        {
          forLabel: "telp",
          icon: "ic:baseline-phone",
          name: "telp",
          placeholder: "Masukan telpon anda..",
          type: "text",
        },
        {
          forLabel: "email",
          icon: "material-symbols:alternate-email",
          name: "email",
          placeholder: "Masukan email anda..",
          type: "text",
        },
        {
          forLabel: "password",
          icon: "carbon:password",
          name: "password",
          placeholder: "Masukan password anda..",
          type: "password",
        },
      ],
    };
  },
};
</script>
