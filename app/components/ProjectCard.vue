<script setup lang="ts">
defineProps<{
  title: string;
  category: string;
  description: string;
  image: string;
}>();
</script>
<template>
  <article class="grid-card-hover h-full">
    <UCard
      class="h-full overflow-hidden rounded-xl border border-zinc-200 shadow-xl"
    >
      <NuxtImg
        :src="image"
        :alt="title"
        class="h-56 w-full rounded-lg object-cover"
        width="960"
        height="640"
        loading="lazy"
      />
      <div class="mt-5 space-y-3">
        <div class="flex items-center justify-between gap-3">
          <h3 class="font-heading text-xl font-bold text-zinc-950">
            {{ title }}
          </h3>
          <UBadge color="primary" variant="soft">
            {{ category }}
          </UBadge>
        </div>
        <p class="text-sm leading-relaxed text-zinc-600">
          {{ description }}
        </p>
      </div>
    </UCard>
  </article>
</template>
