<script setup lang="ts">
const year = new Date().getFullYear();
</script>
<template>
  <footer class="border-t border-brand-900 bg-brand-950 text-slate-100">
    <UContainer class="section-shell py-16">
      <div class="grid gap-10 md:grid-cols-2 xl:grid-cols-4">
        <div class="space-y-4">
          <h3 class="font-heading text-xl font-bold text-white">
            ZBN BRYS Construction Services
          </h3>
          <p class="text-sm leading-relaxed text-slate-300">
            Industrial-grade construction delivery for commercial, civil, and
            infrastructure projects.
          </p>
        </div>

        <div>
          <h4 class="mb-4 font-heading text-base font-semibold text-white">
            Navigation
          </h4>
          <ul class="space-y-2 text-sm text-slate-300">
            <li>
              <NuxtLink to="/" class="hover:text-brand-300">Home</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/about" class="hover:text-brand-300"
                >About</NuxtLink
              >
            </li>
            <li>
              <NuxtLink to="/services" class="hover:text-brand-300"
                >Services</NuxtLink
              >
            </li>
            <li>
              <NuxtLink to="/projects" class="hover:text-brand-300"
                >Projects</NuxtLink
              >
            </li>
            <li>
              <NuxtLink to="/rental-equipment" class="hover:text-brand-300"
                >Rental Equipment</NuxtLink
              >
            </li>
            <li>
              <NuxtLink to="/materials" class="hover:text-brand-300"
                >Materials</NuxtLink
              >
            </li>
            <li>
              <NuxtLink to="/contact" class="hover:text-brand-300"
                >Contact</NuxtLink
              >
            </li>
          </ul>
        </div>

        <div>
          <h4 class="mb-4 font-heading text-base font-semibold text-white">
            Contact
          </h4>
          <ul class="space-y-2 text-sm text-slate-300">
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

      <div class="mt-12 border-t border-brand-900 pt-6 text-sm text-slate-400">
        &copy; {{ year }} ZBN BRYS Construction Services. All rights reserved.
      </div>
    </UContainer>
  </footer>
</template>
