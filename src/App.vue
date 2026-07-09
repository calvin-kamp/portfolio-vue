<script setup lang="ts">
import SiteFooter from './components/layout/SiteFooter.vue'
import SiteHeader from './components/layout/SiteHeader.vue'
</script>

<template>
  <SiteHeader />

  <main>
    <RouterView />
  </main>

  <SiteFooter />
</template>
