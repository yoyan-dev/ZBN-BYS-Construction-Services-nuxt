<script setup lang="ts">
const props = withDefaults(
  defineProps<{
    title: string;
    description?: string;
    eyebrow?: string;
    align?: "left" | "center";
  }>(),
  {
    align: "left",
  },
);

const isCenter = computed(() => props.align === "center");
const alignmentClass = computed(() =>
  isCenter.value ? "text-center" : "text-left",
);
</script>
<template>
  <div :class="['space-y-5', alignmentClass]">
    <UBadge
      v-if="eyebrow"
      color="primary"
      variant="soft"
      class="rounded-full px-4 py-1.5 text-[11px] font-semibold uppercase tracking-[0.22em]"
    >
      {{ eyebrow }}
    </UBadge>
    <h2
      class="font-heading text-3xl font-extrabold leading-tight tracking-tight text-slate-950 sm:text-4xl lg:text-5xl"
    >
      {{ title }}
    </h2>
    <p
      v-if="description"
      class="max-w-3xl text-base leading-relaxed text-slate-600 md:text-lg"
      :class="isCenter ? 'mx-auto' : ''"
    >
      {{ description }}
    </p>
  </div>
</template>
