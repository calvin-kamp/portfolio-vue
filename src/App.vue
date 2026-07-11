<script setup lang="ts">
import { SiteFooter, SiteHeader } from './components/layout'
</script>

<template>
  <SiteHeader />

  <main>
    <RouterView />
  </main>

  <SiteFooter />
</template>
