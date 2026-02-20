<script setup lang="ts">
useHead({
  htmlAttrs: {
    lang: "en",
  },
  meta: [{ name: "viewport", content: "width=device-width, initial-scale=1" }],
  link: [{ rel: "icon", href: "/logo.png" }],
});

const siteTitle = "ZBN BRYS Construction Services";
const siteDescription =
  "Corporate construction services delivering industrial, commercial, and infrastructure projects with safety and precision.";

useSeoMeta({
  title: siteTitle,
  description: siteDescription,
  ogTitle: siteTitle,
  ogDescription: siteDescription,
  twitterCard: "summary_large_image",
});
</script>

<template>
  <UApp>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </UApp>
</template>
