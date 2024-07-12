<script setup lang="ts">
const route = useRoute()
useHead({
  // as a string,
  // where `%s` is replaced with the title
  titleTemplate: '%s | Wise Marketing',
  link: [
    {
      rel: 'canonical',
      href: 'http://localhost:3000' + route.path,
    },
  ]
})
</script>

<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>
