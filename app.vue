<template>
  <div>
    <AppHeader />
    <!-- Page visits: {{ count }} <br /> -->
    <AppAlert> This is an auto-imported component.fff </AppAlert>
    <NuxtPage />
    <AppFooter />
  </div>
</template>

<style>
.page-enter-active,
.page-leave-active {
  transition: all 0.4s;
}
.page-enter-from,
.page-leave-to {
  opacity: 0;
  filter: blur(1rem);
}
</style>
<script setup>
const config = useRuntimeConfig();
console.log(config.API_BASE_URL);
// const { data: count } = await useFetch(`${config.API_BASE_URL}/users`);
// console.log(count.value);
definePageMeta({
  pageTransition: {
    name: "rotate",
  },
});
useHead({
  title: "My App",
  // or, instead:
  // titleTemplate: (title) => `My App - ${title}`,
  viewport: "width=device-width, initial-scale=1, maximum-scale=1",
  charset: "utf-8",
  meta: [{ name: "description", content: "My amazing site." }],
  bodyAttrs: {
    class: "test",
  },
  script: [
    {
      // src: "https://third-party-script.com",
      // body: true,
    },
  ],
});
// const { data } = await useAsyncData(() => $fetch(`${config.API_BASE_URL}/users`));
// console.log(data.value);
</script>
