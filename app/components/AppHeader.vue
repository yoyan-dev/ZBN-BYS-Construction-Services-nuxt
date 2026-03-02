<script setup lang="ts">
const route = useRoute();

const isMobileMenuOpen = ref(false);

const navItems = [
  { label: "Home", to: "/" },
  { label: "About", to: "/about" },
  { label: "Services", to: "/services" },
  { label: "Projects", to: "/projects" },
  { label: "Rental Equipment", to: "/rental-equipment" },
  { label: "Materials", to: "/materials" },
  { label: "Contact", to: "/contact" },
] as const;

const isActive = (path: string) => {
  if (path === "/") {
    return route.path === "/";
  }

  return route.path.startsWith(path);
};
</script>

<template>
  <header
    class="sticky top-0 z-50 border-b border-slate-200/80 bg-white/90 backdrop-blur-xl"
  >
    <div class="h-1 bg-gradient-to-r from-brand-900 via-brand-700 to-brand-500" />

    <UContainer class="section-shell">
      <div class="flex h-20 items-center justify-between gap-6">
        <NuxtLink to="/" class="flex items-center gap-3">
          <div
            class="grid h-11 w-11 place-items-center rounded-xl border border-brand-100 bg-brand-50"
          >
            <NuxtImg src="/logo.png" alt="ZBN BRYS logo" width="400" height="400" />
          </div>
          <div>
            <p
              class="font-heading text-base font-bold tracking-tight text-slate-950"
            >
              ZBN BRYS
            </p>
            <p
              class="text-xs font-semibold uppercase tracking-[0.2em] text-slate-500"
            >
              Construction Services
            </p>
          </div>
        </NuxtLink>

        <nav class="hidden items-center gap-2 md:flex">
          <NuxtLink
            v-for="item in navItems"
            :key="item.to"
            :to="item.to"
            class="rounded-lg px-4 py-2 text-sm font-semibold text-slate-700 transition hover:bg-brand-50 hover:text-brand-800"
            :class="
              isActive(item.to)
                ? 'bg-brand-900 text-white hover:bg-brand-900 hover:text-white'
                : ''
            "
          >
            {{ item.label }}
          </NuxtLink>
        </nav>

        <div class="hidden items-center gap-2 md:flex">
          <UButton size="sm" color="primary" to="/contact">
            Request Quote
          </UButton>
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
      class="border-t border-slate-200 bg-white md:hidden"
    >
      <UContainer class="section-shell py-4">
        <div class="flex flex-col gap-2">
          <NuxtLink
            v-for="item in navItems"
            :key="item.to"
            :to="item.to"
            class="rounded-lg px-4 py-2 text-sm font-semibold text-slate-700 hover:bg-brand-50"
            @click="isMobileMenuOpen = false"
            :class="
              isActive(item.to) ? 'bg-brand-900 text-white hover:bg-brand-900' : ''
            "
          >
            {{ item.label }}
          </NuxtLink>
        </div>
      </UContainer>
    </div>
  </header>
</template>
