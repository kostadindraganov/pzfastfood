<template>
  <main>
    <p v-html="data.menu"></p>
    <!-- <ContentRenderer :value="data">
      <h1>{{ data.menu }}</h1>
      <ContentRendererMarkdown :value="data" />
    </ContentRenderer> -->
  </main>
</template>

<script setup lang="ts">
const { data } = await useAsyncData('menu', () => queryContent('/site/menu').findOne())
</script>
