<script setup lang="ts">
defineProps<{
  title: string;
  description: string;
}>();
</script>

<template>
  <section class="section-wrap pt-4">
    <UContainer class="section-shell">
      <div
        class="relative overflow-hidden rounded-3xl border border-brand-700/70 bg-gradient-to-br from-brand-950 via-brand-900 to-brand-800 px-8 py-12 text-white shadow-2xl md:px-10"
      >
        <div
          class="absolute inset-0 bg-[radial-gradient(circle_at_20%_10%,rgba(147,185,252,0.22),transparent_38%)]"
        />
        <div
          class="relative flex flex-col gap-8 lg:flex-row lg:items-center lg:justify-between"
        >
          <div class="max-w-2xl space-y-4">
            <UBadge
              color="primary"
              variant="solid"
              class="rounded-full px-4 py-1.5 text-[11px] font-semibold uppercase tracking-[0.22em]"
            >
              Ready to Build
            </UBadge>
            <h2
              class="font-heading text-3xl font-extrabold leading-tight text-white sm:text-4xl"
            >
              {{ title }}
            </h2>
            <p class="text-slate-100/90">
              {{ description }}
            </p>
          </div>

          <div class="flex flex-wrap gap-3">
            <UButton size="xl" color="primary" to="/contact">
              Request a Quote
            </UButton>
            <UButton
              size="xl"
              color="neutral"
              variant="outline"
              to="/services"
              class="border-white/35 text-white hover:bg-white/10"
            >
              Review Services
            </UButton>
          </div>
        </div>
      </div>
    </UContainer>
  </section>
</template>
