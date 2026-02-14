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
    title: "Construction Services",
    description:
      "Comprehensive construction solutions including civil, architectural, mechanical, electrical, and plumbing works.",
    badge: "Core Service",
  },
  {
    icon: "i-lucide-package",
    title: "Material Supply",
    description:
      "Reliable supply of quality construction materials and system components for projects of any scale.",
    badge: "Supply",
  },
  {
    icon: "i-lucide-truck",
    title: "Equipment Rental",
    description:
      "Well-maintained construction equipment available for short- and long-term project requirements.",
    badge: "Rental",
  },
];

const projects: ProjectPreview[] = [
  {
    title: "Mid-Rise Commercial Building Project",
    category: "Commercial",
    description:
      "Complete civil, architectural, HVAC, electrical, plumbing, and fire protection system installation for a commercial facility.",
    image:
      "https://images.unsplash.com/photo-1513828583688-c52646db42da?auto=format&fit=crop&w=1200&q=80",
  },
  {
    title: "Industrial Warehouse Development",
    category: "Industrial",
    description:
      "Design and build of an industrial warehouse including power distribution, ventilation systems, and sanitary works.",
    image:
      "https://images.unsplash.com/photo-1504307651254-35680f356dfd?auto=format&fit=crop&w=1200&q=80",
  },
  {
    title: "Institutional Facility System Upgrade",
    category: "Infrastructure",
    description:
      "Retrofitting and system upgrade featuring fire detection, electrical improvements, and HVAC system enhancement.",
    image:
      "https://images.unsplash.com/photo-1473448912268-2022ce9509d8?auto=format&fit=crop&w=1200&q=80",
  },
];

const reasons: ReasonItem[] = [
  {
    icon: "i-lucide-drafting-compass",
    value: "End-to-End",
    title: "Design & Build Expertise",
    description:
      "Integrated engineering and construction solutions from concept planning to project turnover.",
  },
  {
    icon: "i-lucide-shield-check",
    value: "Code-Compliant",
    title: "Regulatory Assurance",
    description:
      "Complete documentation support and strict adherence to industry standards and authority requirements.",
  },
  {
    icon: "i-lucide-cpu",
    value: "Modern Systems",
    title: "Advanced Engineering",
    description:
      "Implementation of HVAC, electrical, fire protection, and plumbing systems using updated technologies.",
  },
  {
    icon: "i-lucide-handshake",
    value: "Client-Focused",
    title: "Collaborative Approach",
    description:
      "Close coordination with clients to balance functionality, efficiency, and cost-effectiveness.",
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
          title="Integrated Construction Services"
          description="From early planning to site execution, our teams provide structured delivery for complex projects."
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
          title="Projects That Define Reliability"
          description="Selected projects showcasing quality, control, and consistent execution across sectors."
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
          title="Why Clients Choose ZBN BRYS"
          description="Measured performance, transparent communication, and long-term partnership focus."
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
