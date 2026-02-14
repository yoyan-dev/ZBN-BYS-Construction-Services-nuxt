<template>
  <section class="relative isolate overflow-hidden">
    <NuxtImg
      src="https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?auto=format&fit=crop&w=1800&q=80"
      alt="Corporate construction skyline"
      class="absolute inset-0 h-full w-full object-cover"
      width="1800"
      height="1100"
      loading="eager"
    />
    <div
      class="absolute inset-0 bg-gradient-to-r from-zinc-950/90 via-zinc-900/75 to-zinc-900/50"
    />

    <UContainer class="relative max-w-7xl mx-auto py-28 lg:py-36">
      <div class="max-w-3xl space-y-7 text-white">
        <UBadge
          color="primary"
          variant="solid"
          class="rounded-full px-4 py-1 text-xs uppercase tracking-[0.2em]"
        >
          Building with Precision
        </UBadge>

        <h1
          class="font-heading text-4xl font-extrabold leading-tight sm:text-5xl lg:text-6xl"
        >
          Build Houses and Settle Down
        </h1>

        <p class="max-w-2xl text-base leading-relaxed text-zinc-200 sm:text-lg">
          Design and build Structural, Architectural, Mechanical, and
          Electronics Works
        </p>

        <div class="flex flex-wrap gap-3">
          <UButton size="xl" color="primary" to="/contact">
            Request Proposal
          </UButton>
          <UButton size="xl" color="neutral" variant="outline" to="/projects">
            View Projects
          </UButton>
        </div>
      </div>
    </UContainer>
  </section>
</template>

<script setup lang="ts">
defineProps<{
  title: string;
  description: string;
}>();
</script>
