<script setup lang="ts">
defineProps<{
  title: string;
  description: string;
}>();
</script>

<template>
  <section class="section-wrap">
    <UContainer class="max-w-7xl mx-auto">
      <div
        class="rounded-3xl border border-amber-100 `bg-linear-to-r from-amber-500 to-amber-400 px-8 py-12 shadow-xl"
      >
        <div
          class="flex flex-col gap-6 md:flex-row md:items-center md:justify-between"
        >
          <div class="max-w-2xl space-y-4">
            <UBadge
              color="neutral"
              variant="solid"
              class="rounded-full bg-zinc-950 text-white"
            >
              Ready to Build
            </UBadge>
            <h2
              class="font-heading text-3xl font-extrabold text-zinc-950 sm:text-4xl"
            >
              {{ title }}
            </h2>
            <p class="text-zinc-800">
              {{ description }}
            </p>
          </div>

          <UButton
            size="xl"
            color="neutral"
            variant="solid"
            to="/contact"
            class="justify-center"
          >
            Talk to Our Team
          </UButton>
        </div>
      </div>
    </UContainer>
  </section>
</template>
