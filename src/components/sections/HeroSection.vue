<script setup lang="ts">
import { ChevronRight, Download } from '@lucide/vue'
import { BaseButton, BaseLink } from '../base'
</script>

<template>
  <section class="relative">
    <div class="flex flex-wrap flex-col gap-6 justify-center h-dvh">
      <figure class="w-30 mx-auto">
        <picture>
          <img class="rounded-full aspect-square" src="https://placehold.co/600x600" alt="alt" />
        </picture>
      </figure>

      <div class="flex flex-col gap-4 text-center">
        <ul class="flex flex-wrap gap-4 justify-center">
          <li class="px-4 py-2 border border-strong rounded-full text-xs">
            Available for full-time
          </li>

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

      <div class="flex flex-wrap gap-6 justify-center">
        <BaseButton :as="BaseLink" href="#projects">
          See My Projects

          <ChevronRight />
        </BaseButton>

        <BaseButton :as="BaseLink" href="www.google.de" download variant="ghost">
          <Download />

          Download CV
        </BaseButton>
      </div>
    </div>

    <svg
      class="absolute inset-1/2 -translate-1/2 -z-1 w-svw h-svh"
      aria-hidden="true"
      xmlns="http://www.w3.org/2000/svg"
      width="100%"
      height="100%"
    >
      <defs>
        <pattern
          id="gridPattern"
          width="32"
          height="32"
          x="50%"
          y="50%"
          patternUnits="userSpaceOnUse"
          patternTransform="translate(-16 -16)"
        >
          <path
            d="M0 .5H31.5V32"
            fill="none"
            stroke="rgb(255, 255, 255, 0.15)"
            stroke-width="1"
            shape-rendering="crispEdges"
          />
        </pattern>

        <radialGradient
          id="gridFade"
          cx="50%"
          cy="50%"
          r="90%"
          gradientUnits="objectBoundingBox"
          gradientTransform="translate(0 0.20) scale(1 0.60)"
        >
          <stop offset="0%" stop-color="var(--text, #e7e5e4)" stop-opacity="1" />
          <stop offset="35%" stop-color="var(--text, #e7e5e4)" stop-opacity="1" />
          <stop offset="52%" stop-color="var(--text, #e7e5e4)" stop-opacity="0.80" />
          <stop offset="64%" stop-color="var(--text, #e7e5e4)" stop-opacity="0.55" />
          <stop offset="74%" stop-color="var(--text, #e7e5e4)" stop-opacity="0.35" />
          <stop offset="82%" stop-color="var(--text, #e7e5e4)" stop-opacity="0.20" />
          <stop offset="89%" stop-color="var(--text, #e7e5e4)" stop-opacity="0.10" />
          <stop offset="94%" stop-color="var(--text, #e7e5e4)" stop-opacity="0.05" />
          <stop offset="100%" stop-color="var(--text, #e7e5e4)" stop-opacity="0" />
        </radialGradient>

        <mask id="fadeMask" mask-type="alpha">
          <rect width="100%" height="100%" fill="url(#gridFade)" />
        </mask>
      </defs>

      <rect width="100%" height="100%" fill="var(--body-background, #0a0a0a)" />
      <rect width="100%" height="100%" fill="url(#gridPattern)" mask="url(#fadeMask)" />
    </svg>
  </section>
</template>
