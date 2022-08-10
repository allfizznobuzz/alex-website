<script setup lang="ts">
// https://github.com/vueuse/head
// you can use this to manipulate the document head in any components,
// they will be rendered correctly in the html results with vite-ssg
useHead({
  title: 'Legal Nurse Elites',
  meta: [
    { name: 'description', content: 'RN services provided for all legal needs' },

  ],
})
</script>

<template>
  <Navigation />
  <RouterView />
  <Footer />
</template>
