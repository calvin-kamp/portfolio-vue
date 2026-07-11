<script setup lang="ts">
const showDialog = defineModel<boolean>()
</script>

<template>
  <dialog v-if="showDialog" :open="showDialog">
    <button @click="showDialog = false">close dialog</button>
  </dialog>
</template>
