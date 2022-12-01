<template>
  <NuxtLayout>
    <Head>
      <Title>Uemkaem.id | Home</Title>
      <Meta name="description" content="Home website uemkaemid Indonesia" />
    </Head>
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
      <Suspense>
        <!-- component card -->
        <CardCerita />

        <!-- end component card -->
        <template #fallback>
          <!-- Loading component -->
          <Loader />
          <!-- end loading component -->
        </template>
      </Suspense>
    </div>
    <Paging />
  </NuxtLayout>
  <DivFooter />
</template>

<script setup></script>
