<template>
  <div>
    <section class="relative overflow-hidden bg-zinc-950 text-white">
      <UContainer class="max-w-7xl mx-auto py-20">
        <div class="max-w-3xl space-y-4">
          <UBadge color="primary" variant="solid">
            About Us
          </UBadge>
          <h1 class="font-heading text-4xl font-extrabold leading-tight sm:text-5xl">
            Built on Trust, Engineered for Performance
          </h1>
          <p class="text-zinc-300">
            ZBN BRYS Construction Services is a corporate construction partner focused on high-value delivery, safety excellence, and long-term client outcomes.
          </p>
        </div>
      </UContainer>
    </section>

    <section class="section-wrap">
      <UContainer class="max-w-7xl mx-auto grid gap-10 lg:grid-cols-2">
        <div class="space-y-5">
          <h2 class="font-heading text-3xl font-bold text-zinc-950">
            Company Introduction
          </h2>
          <p class="text-zinc-600">
            Since our founding, we have delivered industrial and commercial projects with disciplined planning, technical rigor, and transparent collaboration.
          </p>
          <p class="text-zinc-600">
            Our multidisciplinary teams combine project management, engineering execution, and field operations to achieve schedule reliability and quality consistency.
          </p>
        </div>

        <NuxtImg
          src="https://images.unsplash.com/photo-1503387762-592deb58ef4e?auto=format&fit=crop&w=1400&q=80"
          alt="Construction team on project site"
          class="h-full min-h-[320px] w-full rounded-2xl object-cover shadow-xl"
          width="1400"
          height="900"
        />
      </UContainer>
    </section>

    <section class="section-wrap bg-zinc-50">
      <UContainer class="max-w-7xl mx-auto grid gap-6 md:grid-cols-2">
        <UCard class="rounded-xl border border-zinc-200 shadow-xl">
          <h3 class="font-heading text-2xl font-bold text-zinc-950">
            Mission
          </h3>
          <p class="mt-3 text-zinc-600">
            Deliver durable, safe, and cost-efficient construction solutions that create long-term value for clients and communities.
          </p>
        </UCard>

        <UCard class="rounded-xl border border-zinc-200 shadow-xl">
          <h3 class="font-heading text-2xl font-bold text-zinc-950">
            Vision
          </h3>
          <p class="mt-3 text-zinc-600">
            Be the most trusted construction services partner for complex projects requiring precision, accountability, and innovation.
          </p>
        </UCard>
      </UContainer>
    </section>

    <section class="section-wrap">
      <UContainer class="max-w-7xl mx-auto space-y-8">
        <SectionTitle
          eyebrow="Timeline"
          title="Key Company Milestones"
          description="A snapshot of our growth and project capability expansion."
        />

        <div class="space-y-4">
          <UCard v-for="item in timeline" :key="item.year" class="rounded-xl border border-zinc-200 shadow-xl">
            <div class="flex flex-col gap-2 md:flex-row md:items-center md:gap-6">
              <UBadge color="primary" variant="soft" class="w-fit">
                {{ item.year }}
              </UBadge>
              <h3 class="font-heading text-lg font-semibold text-zinc-950">
                {{ item.title }}
              </h3>
            </div>
            <p class="mt-3 text-zinc-600">
              {{ item.description }}
            </p>
          </UCard>
        </div>
      </UContainer>
    </section>

    <section class="section-wrap bg-zinc-950 text-white">
      <UContainer class="max-w-7xl mx-auto grid gap-8 lg:grid-cols-[1.4fr_1fr] lg:items-center">
        <div class="space-y-4">
          <UBadge color="primary" variant="solid">
            Safety Commitment
          </UBadge>
          <h2 class="font-heading text-3xl font-extrabold sm:text-4xl">
            Every Project Begins with Safety
          </h2>
          <p class="text-zinc-300">
            Our safety programs include daily briefings, method statements, risk reviews, and continuous training to protect every person onsite.
          </p>
        </div>

        <UCard class="rounded-xl border border-zinc-700 bg-zinc-900 shadow-xl">
          <ul class="space-y-3 text-zinc-200">
            <li class="flex items-start gap-3">
              <UIcon name="i-lucide-check-circle-2" class="mt-0.5 h-5 w-5 text-amber-400" />
              OSHA-aligned procedures and documented compliance checks
            </li>
            <li class="flex items-start gap-3">
              <UIcon name="i-lucide-check-circle-2" class="mt-0.5 h-5 w-5 text-amber-400" />
              Dedicated site safety leads for active projects
            </li>
            <li class="flex items-start gap-3">
              <UIcon name="i-lucide-check-circle-2" class="mt-0.5 h-5 w-5 text-amber-400" />
              Tool-box talks and recurring emergency response drills
            </li>
          </ul>
        </UCard>
      </UContainer>
    </section>
  </div>
</template>

<script setup lang="ts">
interface TimelineItem {
  year: string
  title: string
  description: string
}

const timeline: TimelineItem[] = [
  {
    year: '2008',
    title: 'Company Founded',
    description: 'Started as a focused contractor for regional industrial clients.'
  },
  {
    year: '2013',
    title: 'Commercial Expansion',
    description: 'Expanded into commercial construction with dedicated project management teams.'
  },
  {
    year: '2018',
    title: 'Infrastructure Division Launch',
    description: 'Introduced infrastructure services for transportation and public-sector projects.'
  },
  {
    year: '2024',
    title: 'Digital Site Operations',
    description: 'Adopted digital reporting and BIM-supported workflows across all major projects.'
  }
]
</script>
