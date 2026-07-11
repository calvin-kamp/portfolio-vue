<script setup lang="ts">
import { BaseLink } from '../base'

interface NavItem {
  href: string
  label: string
}

const footerNavigation: NavItem[] = [
  { href: 'https://github.com/calvin-kamp', label: 'GitHub' },
  { href: 'https://github.com/calvin-kamp', label: 'LinkedIn' },
  { href: '/imprint', label: 'Impressum' },
]

const currentYear = new Date().getFullYear()
</script>

<template>
  <footer class="py-3 flex flex-wrap gap-3 justify-center">
    <nav class="w-full">
      <ul class="flex flex-wrap gap-3 justify-center">
        <li v-for="navItem in footerNavigation" :key="navItem.href">
          <BaseLink :href="navItem.href">
            {{ navItem.label }}
          </BaseLink>
        </li>
      </ul>
    </nav>

    <p>{{ currentYear }} Calvin Kamp</p>
  </footer>
</template>
