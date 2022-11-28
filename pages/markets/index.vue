<template>
  <NuxtLayout>
    <Head>
      <Title>Uemkaem.id | Marketsplace</Title>
      <Meta name="description" content="Home website uemkaemid Indonesia" />
    </Head>
    <h1>Ini Markets</h1>
  </NuxtLayout>
</template>

<script setup lang="ts">
// import data form data makets-store.json nuxt
import markets from "assets/data/markets-store.json";

const store = ref(markets);
console.log(store.value.products.length);
</script>
