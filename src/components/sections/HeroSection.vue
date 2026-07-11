<script setup lang="ts">
import { ChevronRight, Download } from '@lucide/vue'
import { BaseLink } from '../base'
</script>

<template>
  <section class="h-dvh flex flex-wrap flex-col gap-6 justify-center">
    <figure class="w-30 mx-auto">
      <picture>
        <img class="rounded-full aspect-square" src="https://placehold.co/600x600" alt="alt" />
      </picture>
    </figure>

    <div class="flex flex-col gap-4 text-center">
      <ul class="flex gap-4 justify-center">
        <li class="px-4 py-2 border border-strong rounded-full text-xs">Available for full-time</li>
        <li class="px-4 py-2 border border-strong rounded-full text-xs">Hagen - Remote</li>
      </ul>

      <h1 class="text-pretty text-3xl md:text-5xl lg:text-6xl">
        <span class="text-primary"> Frontend </span>
        &
        <span class="text-primary"> Accessibility </span>
        Synergy
      </h1>

      <p>
        <span class="block"> Hi, I'm Calvin </span>

        I create modern frontends that are accessible, easy to use, and built with attention to
        detail.
      </p>
    </div>

    <div class="flex flex-wrap gap-6">
      <BaseLink href="#projects">
        See My Projects

        <ChevronRight />
      </BaseLink>

      <BaseLink href="www.google.de">
        <Download />

        Download CV
      </BaseLink>
    </div>
  </section>
</template>
