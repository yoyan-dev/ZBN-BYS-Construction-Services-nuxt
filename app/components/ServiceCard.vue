<template>
  <article class="grid-card-hover h-full">
    <UCard class="h-full rounded-xl border border-zinc-200 shadow-xl">
      <div class="mb-5 flex items-center justify-between">
        <div
          class="grid h-12 w-12 place-items-center rounded-xl bg-amber-100 text-amber-700"
        >
          <UIcon :name="icon" class="h-6 w-6" />
        </div>
        <UBadge v-if="badge" color="neutral" variant="subtle">
          {{ badge }}
        </UBadge>
      </div>
      <h3 class="font-heading text-xl font-bold text-zinc-950">
        Integrated Construction Services
      </h3>
      <p class="mt-3 text-sm leading-relaxed text-zinc-600">
        From early planning to site execution, our teams provide structured
        delivery for complex projects.
      </p>
    </UCard>
  </article>
</template>

<script setup lang="ts">
defineProps<{
  icon: string;
  title: string;
  description: string;
  badge?: string;
}>();
</script>
