<script setup lang="ts">
interface HeroMetric {
  value: string;
  label: string;
}

withDefaults(
  defineProps<{
    title: string;
    description: string;
    metrics?: HeroMetric[];
  }>(),
  {
    metrics: () => [
      {
        value: "18+",
        label: "Years Experience",
      },
      {
        value: "320+",
        label: "Projects Delivered",
      },
      {
        value: "ISO-Ready",
        label: "Compliance Focus",
      },
    ],
  },
);
</script>
<template>
  <section class="relative isolate overflow-hidden">
    <NuxtImg
      src="/images/IMG_2518.jpeg"
      alt="Corporate construction project skyline"
      class="absolute inset-0 h-full w-full object-cover"
      width="1800"
      height="1100"
      loading="eager"
    />
    <div
      class="absolute inset-0 bg-gradient-to-r from-brand-950/95 via-brand-900/85 to-brand-900/60"
    />
    <div
      class="absolute inset-0 bg-[radial-gradient(circle_at_85%_8%,rgba(147,185,252,0.2),transparent_40%)]"
    />

    <UContainer class="section-shell relative py-24 lg:py-32">
      <div class="grid gap-10 lg:grid-cols-[1.1fr_0.9fr] lg:items-end">
        <div class="space-y-8 text-white">
          <UBadge
            color="primary"
            variant="solid"
            class="rounded-full px-4 py-1.5 text-[11px] font-semibold uppercase tracking-[0.22em]"
          >
            Engineering-Driven Construction
          </UBadge>

          <h1
            class="font-heading max-w-4xl text-4xl font-extrabold leading-tight sm:text-5xl lg:text-6xl"
          >
            {{ title }}
          </h1>

          <p
            class="max-w-2xl text-base leading-relaxed text-slate-100/90 sm:text-lg"
          >
            {{ description }}
          </p>

          <div class="flex flex-wrap gap-4">
            <UButton size="xl" color="primary" to="/contact">
              Get a Free Estimate
            </UButton>
            <UButton
              size="xl"
              color="neutral"
              variant="outline"
              to="/projects"
              class="border-white/35 text-white hover:bg-white/10"
            >
              View Projects
            </UButton>
          </div>

          <div class="grid gap-3 sm:grid-cols-3">
            <div
              v-for="metric in metrics"
              :key="metric.label"
              class="rounded-xl border border-white/20 bg-white/10 px-4 py-4 backdrop-blur-sm"
            >
              <p class="font-heading text-2xl font-bold text-white">
                {{ metric.value }}
              </p>
              <p class="text-xs font-medium uppercase tracking-[0.14em] text-white/80">
                {{ metric.label }}
              </p>
            </div>
          </div>
        </div>

        <UCard
          class="rounded-2xl border border-white/15 bg-white/10 text-white shadow-2xl backdrop-blur-sm"
        >
          <h2 class="font-heading text-2xl font-bold">
            Trusted for Commercial and Industrial Builds
          </h2>
          <p class="mt-3 text-sm leading-relaxed text-white/85">
            We combine disciplined planning, coordinated trades, and quality
            controls to deliver projects with schedule certainty.
          </p>

          <ul class="mt-6 space-y-3 text-sm text-white/90">
            <li class="flex items-start gap-3">
              <UIcon
                name="i-lucide-check-circle-2"
                class="mt-0.5 h-5 w-5 text-brand-300"
              />
              Transparent reporting with milestone-based updates
            </li>
            <li class="flex items-start gap-3">
              <UIcon
                name="i-lucide-check-circle-2"
                class="mt-0.5 h-5 w-5 text-brand-300"
              />
              Dedicated technical leads for every discipline
            </li>
            <li class="flex items-start gap-3">
              <UIcon
                name="i-lucide-check-circle-2"
                class="mt-0.5 h-5 w-5 text-brand-300"
              />
              Compliance-ready documentation and site safety programs
            </li>
          </ul>
        </UCard>
      </div>
    </UContainer>
  </section>
</template>
