<script setup lang="ts">
import { computed } from 'vue'
import { RouterLink } from 'vue-router'

interface Props {
  href: string
  name?: string
}

const props = defineProps<Props>()

const isInternal = computed((): boolean => props.name !== undefined || props.href.startsWith('#'))
</script>

<template>
  <RouterLink v-if="isInternal" :to="name ?? href">
    <slot />
  </RouterLink>

  <a v-else :href="href" target="_blank" rel="noopener noreferrer">
    <slot />
  </a>
</template>
