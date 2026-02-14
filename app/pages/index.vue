<script setup lang="ts">
import { useI18n } from "#imports";

const { t } = useI18n();

interface ServicePreview {
  icon: string;
  title: string;
  description: string;
  badge: string;
}

interface ProjectPreview {
  title: string;
  category: string;
  description: string;
  image: string;
}

interface ReasonItem {
  icon: string;
  value: string;
  title: string;
  description: string;
}

const services: ServicePreview[] = [
  {
    icon: "i-lucide-building-2",
    title: "Commercial Construction",
    description:
      "Office and mixed-use developments built for durability and operational efficiency.",
    badge: "Turnkey",
  },
  {
    icon: "i-lucide-factory",
    title: "Industrial Facilities",
    description:
      "High-performance plants, warehouses, and logistics hubs optimized for throughput.",
    badge: "Industrial",
  },
  {
    icon: "i-lucide-shield-check",
    title: "Structural Rehabilitation",
    description:
      "Specialized retrofit and reinforcement programs extending lifecycle and resilience.",
    badge: "Safety-First",
  },
];

const projects: ProjectPreview[] = [
  {
    title: "Northpoint Logistics Hub",
    category: "Industrial",
    description:
      "420,000 sq ft logistics platform delivered in 16 months with zero lost-time incidents.",
    image:
      "https://images.unsplash.com/photo-1513828583688-c52646db42da?auto=format&fit=crop&w=1200&q=80",
  },
  {
    title: "Rivergate Business Center",
    category: "Commercial",
    description:
      "High-rise office campus with integrated smart-building controls and LEED-ready systems.",
    image:
      "https://images.unsplash.com/photo-1504307651254-35680f356dfd?auto=format&fit=crop&w=1200&q=80",
  },
  {
    title: "Eastline Bridge Reinforcement",
    category: "Infrastructure",
    description:
      "Critical transport corridor upgrade completed under active traffic management.",
    image:
      "https://images.unsplash.com/photo-1473448912268-2022ce9509d8?auto=format&fit=crop&w=1200&q=80",
  },
];

const reasons: ReasonItem[] = [
  {
    icon: "i-lucide-hard-hat",
    value: "18+ Years",
    title: "Proven Experience",
    description:
      "Regional and national project expertise across multiple construction disciplines.",
  },
  {
    icon: "i-lucide-shield",
    value: "100%",
    title: "Safety Culture",
    description:
      "Comprehensive compliance protocols and workforce training embedded at every level.",
  },
  {
    icon: "i-lucide-clock-3",
    value: "On Schedule",
    title: "Delivery Discipline",
    description:
      "Lean planning and transparent reporting to keep milestones predictable.",
  },
  {
    icon: "i-lucide-handshake",
    value: "Client First",
    title: "Partnership Model",
    description:
      "Collaborative engagement model with clear communication from bid to handover.",
  },
];
</script>

<template>
  <div>
    <HeroSection
      :title="t('home.hero.title')"
      :description="t('home.hero.description')"
    />

    <section class="section-wrap">
      <UContainer class="max-w-7xl mx-auto space-y-12">
        <SectionTitle
          eyebrow="Core Services"
          :title="t('home.services.title')"
          :description="t('home.services.description')"
          align="center"
        />

        <div class="grid gap-6 md:grid-cols-2 xl:grid-cols-3">
          <ServiceCard
            v-for="service in services"
            :key="service.title"
            :icon="service.icon"
            :title="service.title"
            :description="service.description"
            :badge="service.badge"
          />
        </div>
      </UContainer>
    </section>

    <section class="section-wrap bg-zinc-50">
      <UContainer class="max-w-7xl mx-auto space-y-12">
        <SectionTitle
          eyebrow="Featured Work"
          :title="t('home.projects.title')"
          :description="t('home.projects.description')"
          align="center"
        />

        <div class="grid gap-6 md:grid-cols-2 xl:grid-cols-3">
          <ProjectCard
            v-for="project in projects"
            :key="project.title"
            :title="project.title"
            :category="project.category"
            :description="project.description"
            :image="project.image"
          />
        </div>
      </UContainer>
    </section>

    <section class="section-wrap">
      <UContainer class="max-w-7xl mx-auto space-y-10">
        <SectionTitle
          eyebrow="Why ZBN BRYS"
          :title="t('home.why.title')"
          :description="t('home.why.description')"
          align="center"
        />

        <div class="grid gap-6 md:grid-cols-2 xl:grid-cols-4">
          <UCard
            v-for="item in reasons"
            :key="item.title"
            class="rounded-xl border border-zinc-200 shadow-xl"
          >
            <UIcon :name="item.icon" class="h-8 w-8 text-amber-500" />
            <p class="mt-4 font-heading text-2xl font-bold text-zinc-950">
              {{ item.value }}
            </p>
            <h3 class="mt-2 font-heading text-lg font-semibold text-zinc-900">
              {{ item.title }}
            </h3>
            <p class="mt-2 text-sm text-zinc-600">
              {{ item.description }}
            </p>
          </UCard>
        </div>
      </UContainer>
    </section>

    <CTASection
      title="Start Your Next Project with a Trusted Construction Partner"
      description="From planning to turnover, our team delivers schedule certainty, safety compliance, and premium execution quality."
    />
  </div>
</template>
