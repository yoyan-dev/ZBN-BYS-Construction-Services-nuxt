<script setup lang="ts">
defineProps<{
  title: string;
  category: string;
  description: string;
  image: string;
}>();
</script>
<template>
  <article class="group grid-card-hover h-full">
    <UCard
      class="h-full overflow-hidden rounded-2xl border border-slate-200 bg-white p-0 shadow-sm ring-1 ring-brand-100/40 transition group-hover:border-brand-200"
    >
      <div class="relative overflow-hidden">
        <NuxtImg
          :src="image"
          :alt="title"
          class="h-60 w-full object-cover transition-transform duration-500 group-hover:scale-105"
          width="960"
          height="640"
          loading="lazy"
        />
        <div
          class="absolute inset-0 bg-gradient-to-t from-brand-950/85 via-brand-900/20 to-transparent"
        />
        <div class="absolute inset-x-4 bottom-4 flex items-center justify-between gap-3">
          <UBadge
            color="primary"
            variant="solid"
            class="rounded-full px-3 py-1 text-[11px] font-semibold uppercase tracking-[0.18em]"
          >
            {{ category }}
          </UBadge>
          <span
            class="grid h-9 w-9 place-items-center rounded-full border border-white/45 bg-white/15 text-white backdrop-blur-sm"
          >
            <UIcon name="i-lucide-arrow-up-right" class="h-4 w-4" />
          </span>
        </div>
      </div>
      <div class="space-y-3 p-6">
        <h3 class="font-heading text-xl font-bold text-slate-950">
          {{ title }}
        </h3>
        <p class="text-sm leading-relaxed text-slate-600">
          {{ description }}
        </p>
      </div>
    </UCard>
  </article>
</template>
