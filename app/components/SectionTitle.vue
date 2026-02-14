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
  <div :class="['space-y-4', alignmentClass]">
    <UBadge
      v-if="eyebrow"
      color="primary"
      variant="soft"
      class="rounded-full px-3 py-1 uppercase tracking-[0.16em]"
    >
      {{ eyebrow }}
    </UBadge>
    <h2
      class="font-heading text-3xl font-bold tracking-tight text-zinc-950 sm:text-4xl"
    >
      {{ title }}
    </h2>
    <p
      v-if="description"
      class="max-w-3xl text-zinc-600"
      :class="isCenter ? 'mx-auto' : ''"
    >
      {{ description }}
    </p>
  </div>
</template>
