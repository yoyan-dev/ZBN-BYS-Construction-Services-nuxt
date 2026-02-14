<template>
  <section class="section-wrap">
    <UContainer class="max-w-7xl mx-auto space-y-12">
      <SectionTitle
        eyebrow="Our Services"
        title="Specialized Construction Services"
        description="Comprehensive execution capabilities across industrial, commercial, and infrastructure domains."
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
</template>

<script setup lang="ts">
interface ServiceItem {
  icon: string
  title: string
  description: string
  badge: string
}

const services: ServiceItem[] = [
  {
    icon: 'i-lucide-building',
    title: 'General Contracting',
    description: 'End-to-end project execution from planning through turnover with integrated delivery controls.',
    badge: 'Core'
  },
  {
    icon: 'i-lucide-hammer',
    title: 'Structural Works',
    description: 'Concrete, steel, and hybrid structural systems engineered for reliability and performance.',
    badge: 'Engineering'
  },
  {
    icon: 'i-lucide-factory',
    title: 'Industrial Buildouts',
    description: 'Process-ready facilities and plant expansions tailored to high-output operations.',
    badge: 'Industrial'
  },
  {
    icon: 'i-lucide-crane',
    title: 'Heavy Civil',
    description: 'Civil infrastructure upgrades including roads, utility corridors, and support structures.',
    badge: 'Infrastructure'
  },
  {
    icon: 'i-lucide-shield-check',
    title: 'Safety Management',
    description: 'Comprehensive risk mitigation and compliance monitoring integrated into every phase.',
    badge: 'Compliance'
  },
  {
    icon: 'i-lucide-wrench',
    title: 'Maintenance & Retrofit',
    description: 'Lifecycle extension services for aging assets with minimal operational disruption.',
    badge: 'Lifecycle'
  }
]
</script>
