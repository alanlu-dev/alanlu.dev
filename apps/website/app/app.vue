<script lang="ts" setup>
useHead({
  htmlAttrs: {
    id: 'mcss',
  },
  bodyAttrs: {
    class: 'normal fg:base-fg bg:base-bg overflow-x:hidden',
  },
  script: [
    {
      src: 'https://rybbit.alanlu.dev/api/script.js?siteId=1',
      defer: true,
    },
  ],
})

const CSSRuntimeProvider = defineAsyncComponent(async () => (await import('@master/css.vue')).CSSRuntimeProvider)
</script>

<template>
  <CSSRuntimeProvider :config="import('./master.css.mjs')">
    <NuxtLayout>
      <NuxtLoadingIndicator />
      <ModalsContainer />
      <NuxtPage />
    </NuxtLayout>
  </CSSRuntimeProvider>
</template>
