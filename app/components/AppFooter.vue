<script setup lang="ts">
const year = new Date().getFullYear();
</script>
<template>
  <footer class="border-t border-zinc-800 bg-zinc-950 text-zinc-100">
    <UContainer class="max-w-7xl mx-auto py-16">
      <div class="grid gap-10 md:grid-cols-2 xl:grid-cols-4">
        <div class="space-y-4">
          <h3 class="font-heading text-xl font-bold text-white">
            ZBN BRYS Construction Services
          </h3>
          <p class="text-sm leading-relaxed text-zinc-300">
            Industrial-grade construction delivery for commercial, civil, and
            infrastructure projects.
          </p>
        </div>

        <div>
          <h4 class="mb-4 font-heading text-base font-semibold text-white">
            Navigation
          </h4>
          <ul class="space-y-2 text-sm text-zinc-300">
            <li>
              <NuxtLink to="/" class="hover:text-amber-400">Home</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/about" class="hover:text-amber-400"
                >About</NuxtLink
              >
            </li>
            <li>
              <NuxtLink to="/services" class="hover:text-amber-400"
                >Services</NuxtLink
              >
            </li>
            <li>
              <NuxtLink to="/projects" class="hover:text-amber-400"
                >Projects</NuxtLink
              >
            </li>
            <li>
              <NuxtLink to="/rental-equipment" class="hover:text-amber-400"
                >Rental Equipment</NuxtLink
              >
            </li>
            <li>
              <NuxtLink to="/materials" class="hover:text-amber-400"
                >Materials</NuxtLink
              >
            </li>
            <li>
              <NuxtLink to="/contact" class="hover:text-amber-400"
                >Contact</NuxtLink
              >
            </li>
          </ul>
        </div>

        <div>
          <h4 class="mb-4 font-heading text-base font-semibold text-white">
            Contact
          </h4>
          <ul class="space-y-2 text-sm text-zinc-300">
            <li>+639-489-1200</li>
            <li>zbnbrysconstruction@gmail.com</li>
            <li>Lapu Lapu City, Cebu Philippines</li>
          </ul>
        </div>

        <div>
          <h4 class="mb-4 font-heading text-base font-semibold text-white">
            Newsletter
          </h4>
          <div class="space-y-3">
            <UInput
              placeholder="Work email"
              color="neutral"
              variant="outline"
            />
            <UButton color="primary" class="w-full justify-center">
              Subscribe
            </UButton>
          </div>
        </div>
      </div>

      <div class="mt-12 border-t border-zinc-800 pt-6 text-sm text-zinc-400">
        (c) {{ year }} ZBN BRYS Construction Services. All rights reserved.
      </div>
    </UContainer>
  </footer>
</template>
