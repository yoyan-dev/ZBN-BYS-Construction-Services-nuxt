<template>
  <header
    class="sticky top-0 z-50 border-b border-zinc-200/70 bg-white/95 backdrop-blur"
  >
    <UContainer class="max-w-7xl mx-auto">
      <div class="flex h-20 items-center justify-between gap-6">
        <NuxtLink to="/" class="flex items-center gap-3">
          <div class="grid h-11 w-11 place-items-center">
            <NuxtImg src="/logo.png" alt="image" width="400" height="400" />
          </div>
          <div>
            <p
              class="font-heading text-base font-bold tracking-tight text-zinc-950"
            >
              ZBN BRYS
            </p>
            <p
              class="text-xs font-semibold uppercase tracking-[0.2em] text-zinc-500"
            >
              Construction Services
            </p>
          </div>
        </NuxtLink>

        <nav class="hidden items-center gap-2 md:flex">
          <NuxtLink
            v-for="item in navItems"
            :key="item.key"
            :to="item.to"
            class="rounded-lg px-4 py-2 text-sm font-semibold transition hover:bg-zinc-100 hover:text-zinc-950"
            :class="
              isActive(item.to)
                ? 'bg-zinc-900 text-white hover:bg-zinc-900 hover:text-white'
                : ''
            "
          >
            {{ item.key }}
          </NuxtLink>
        </nav>

        <div class="hidden items-center gap-2 md:flex">
          <UButton size="sm" color="primary" to="/contact"> Get Quote </UButton>
        </div>

        <UButton
          class="md:hidden"
          color="neutral"
          variant="outline"
          icon="i-lucide-menu"
          aria-label="Toggle menu"
          @click="isMobileMenuOpen = !isMobileMenuOpen"
        />
      </div>
    </UContainer>

    <div
      v-if="isMobileMenuOpen"
      class="border-t border-zinc-200 bg-white md:hidden"
    >
      <UContainer class="max-w-7xl mx-auto py-4">
        <div class="flex flex-col gap-2">
          <NuxtLink
            v-for="item in navItems"
            :key="item.key"
            :to="item.to"
            class="rounded-lg px-4 py-2 text-sm font-semibold text-zinc-700 hover:bg-zinc-100"
            @click="isMobileMenuOpen = false"
          >
            {{ item.key }}
          </NuxtLink>
          <div class="mt-2 flex gap-2">
            <UButton
              v-for="code in localeCodes"
              :key="code"
              size="sm"
              :variant="locale === code ? 'solid' : 'outline'"
              :color="locale === code ? 'primary' : 'neutral'"
              @click="setLocale(code)"
            >
              {{ code.toUpperCase() }}
            </UButton>
          </div>
        </div>
      </UContainer>
    </div>
  </header>
</template>

<script setup lang="ts">
import { useI18n } from "#imports";

const { t, locale, locales, setLocale } = useI18n();
const route = useRoute();

const isMobileMenuOpen = ref(false);

const navItems = [
  { key: "home", to: "/" },
  { key: "about", to: "/about" },
  { key: "services", to: "/services" },
  { key: "projects", to: "/projects" },
  { key: "contact", to: "/contact" },
] as const;

const localeCodes = computed(() => locales.value.map((item) => item.code));

const isActive = (path: string) => {
  if (path === "/") {
    return route.path === "/";
  }

  return route.path.startsWith(path);
};
</script>
