<script setup lang="ts">
import type { NavItem } from '.'
import { BaseButton, BaseLink } from '../base'
import { ContactRound, FolderGit2, Home, UserRound, type LucideIcon } from '@lucide/vue'

interface HeaderNavItem extends NavItem {
  icon: LucideIcon
}

const headerNavigation: HeaderNavItem[] = [
  { href: '#home', label: 'Home', icon: Home },
  { href: '#about', label: 'About', icon: UserRound },
  { href: '#projects', label: 'Projects', icon: FolderGit2 },
  { href: '#contact', label: 'Contact', icon: ContactRound },
]
</script>
<template>
  <header
    class="fixed top-6 left-1/2 -translate-x-1/2 py-2 px-6 bg-surface border border-border rounded-full z-10"
  >
    <nav>
      <ul class="flex gap-6 align-center">
        <li class="" v-for="navItem in headerNavigation" :key="navItem.href">
          <BaseButton :href="navItem.href" :as="BaseLink" variant="ghost" size="icon">
            <component :is="navItem.icon" class="size-5" aria-hidden="true" />

            <span class="sr-only lg:not-sr-only">
              {{ navItem.label }}
            </span>
          </BaseButton>
        </li>
      </ul>
    </nav>
  </header>
</template>
