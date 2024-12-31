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
      'src': 'https://plausible.alanlu.dev/js/script.file-downloads.hash.outbound-links.pageview-props.tagged-events.js',
      'data-domain': 'alanlu.dev',
      'defer': true,
    },
    { children: 'window.plausible = window.plausible || function() { (window.plausible.q = window.plausible.q || []).push(arguments) }' },
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
