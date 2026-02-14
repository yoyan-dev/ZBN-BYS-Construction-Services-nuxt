<template>
  <section class="section-wrap">
    <UContainer class="max-w-7xl mx-auto space-y-12">
      <SectionTitle
        eyebrow="Contact"
        title="Let's Plan Your Next Construction Project"
        description="Share your requirements and our team will prepare a tailored construction proposal."
        align="center"
      />

      <div class="grid gap-8 lg:grid-cols-[1.2fr_1fr]">
        <UCard class="rounded-xl border border-zinc-200 shadow-xl">
          <FormKit
            type="form"
            :actions="false"
            @submit="onSubmit"
          >
            <div class="grid gap-4 md:grid-cols-2">
              <FormKit
                type="text"
                name="firstName"
                label="First Name"
                placeholder="John"
                validation="required"
              />
              <FormKit
                type="text"
                name="lastName"
                label="Last Name"
                placeholder="Carter"
                validation="required"
              />
            </div>

            <div class="mt-4 grid gap-4 md:grid-cols-2">
              <FormKit
                type="email"
                name="email"
                label="Work Email"
                placeholder="john@company.com"
                validation="required|email"
              />
              <FormKit
                type="text"
                name="phone"
                label="Phone"
                placeholder="+1 (555) 123-4567"
              />
            </div>

            <div class="mt-4">
              <FormKit
                type="text"
                name="company"
                label="Company"
                placeholder="Your company name"
              />
            </div>

            <div class="mt-4">
              <FormKit
                type="textarea"
                name="message"
                label="Project Details"
                placeholder="Tell us about scope, timelines, and location..."
                validation="required|length:20,800"
              />
            </div>

            <div class="mt-6">
              <UButton type="submit" size="lg" color="primary">
                Submit Inquiry
              </UButton>
            </div>
          </FormKit>
        </UCard>

        <div class="space-y-6">
          <UCard class="rounded-xl border border-zinc-200 shadow-xl">
            <h3 class="font-heading text-xl font-bold text-zinc-950">
              Contact Information
            </h3>
            <ul class="mt-4 space-y-3 text-sm text-zinc-600">
              <li class="flex items-center gap-3">
                <UIcon name="i-lucide-phone-call" class="h-5 w-5 text-amber-500" />
                +1 (555) 489-1200
              </li>
              <li class="flex items-center gap-3">
                <UIcon name="i-lucide-mail" class="h-5 w-5 text-amber-500" />
                hello@zbnbrys.com
              </li>
              <li class="flex items-center gap-3">
                <UIcon name="i-lucide-map-pin" class="h-5 w-5 text-amber-500" />
                1120 Industrial Ave, Houston, TX
              </li>
            </ul>
          </UCard>

          <UCard class="rounded-xl border border-zinc-200 shadow-xl">
            <h3 class="font-heading text-xl font-bold text-zinc-950">
              Quick Notes
            </h3>
            <p class="mt-2 text-sm text-zinc-600">
              UI-only notes field for internal prototyping.
            </p>
            <div class="mt-4 space-y-3">
              <UInput placeholder="Project code" />
              <UTextarea :rows="4" placeholder="Additional notes..." />
            </div>
          </UCard>

          <UCard class="rounded-xl border border-zinc-200 shadow-xl">
            <h3 class="font-heading text-xl font-bold text-zinc-950">
              Location
            </h3>
            <div class="mt-4 grid h-56 place-items-center rounded-xl border border-dashed border-zinc-300 bg-zinc-100 text-sm text-zinc-500">
              Map Placeholder
            </div>
          </UCard>
        </div>
      </div>
    </UContainer>
  </section>
</template>

<script setup lang="ts">
const onSubmit = (_payload: Record<string, unknown>) => {
  // UI-only placeholder: no backend submission in this implementation.
}
</script>

