<script setup lang="ts">
defineProps<{
  icon: string;
  title: string;
  description: string;
  badge?: string;
}>();
</script>
<template>
  <article class="group grid-card-hover h-full">
    <UCard
      class="h-full rounded-2xl border border-slate-200 bg-white shadow-sm ring-1 ring-brand-100/40 transition group-hover:border-brand-200"
    >
      <div class="mb-6 flex items-center justify-between">
        <div
          class="grid h-12 w-12 place-items-center rounded-xl bg-brand-100 text-brand-700 shadow-sm"
        >
          <UIcon :name="icon" class="h-6 w-6" />
        </div>
        <UBadge
          v-if="badge"
          color="primary"
          variant="soft"
          class="rounded-full px-3 py-1 text-[11px] font-semibold uppercase tracking-[0.18em]"
        >
          {{ badge }}
        </UBadge>
      </div>
      <h3 class="font-heading text-xl font-bold text-slate-950">
        {{ title }}
      </h3>
      <p class="mt-3 text-sm leading-relaxed text-slate-600">
        {{ description }}
      </p>
      <div class="mt-6 flex items-center gap-2 text-sm font-semibold text-brand-700">
        <span>Learn More</span>
        <UIcon
          name="i-lucide-arrow-right"
          class="h-4 w-4 transition-transform duration-300 group-hover:translate-x-1"
        />
      </div>
    </UCard>
  </article>
</template>
