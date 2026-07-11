<script setup lang="ts">
import { computed, type HTMLAttributes } from 'vue'

interface Props {
  class?: HTMLAttributes['class']
  variant?: 'primary' | 'ghost'
}

const props = withDefaults(defineProps<Props>(), {
  variant: 'primary',
})

const variantClasses = computed((): string => (props.variant === 'primary' ? '' : ''))
</script>

<template>
  <button
    :class="variantClasses"
    class="inline-flex gap-md justify-center px-5 py-2 rounded-xl outline-none ring-ring focus:ring-2 focus:ring-offset-2"
  >
    <slot />
  </button>
</template>
