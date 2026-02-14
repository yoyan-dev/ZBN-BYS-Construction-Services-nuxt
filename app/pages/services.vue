<script setup lang="ts">
interface ServiceItem {
  icon: string;
  title: string;
  description: string;
  badge: string;
}

const services: ServiceItem[] = [
  {
    icon: "i-lucide-drafting-compass",
    title: "Design and Build",
    description:
      "Complete project delivery from concept design, planning, and engineering through full construction and turnover.",
    badge: "Core",
  },
  {
    icon: "i-lucide-bell-ring",
    title: "Fire Detection Alarm System",
    description:
      "Supply and installation of reliable fire detection and alarm systems compliant with safety standards.",
    badge: "Fire Safety",
  },
  {
    icon: "i-lucide-wind",
    title: "HVAC System",
    description:
      "Ventilation, ducting, chilled water, AC, and VRF systems for commercial and industrial facilities.",
    badge: "Mechanical",
  },
  {
    icon: "i-lucide-zap",
    title: "Electrical Works",
    description:
      "Commercial and industrial power systems including panel boards, wiring, and distribution systems.",
    badge: "Electrical",
  },
  {
    icon: "i-lucide-droplets",
    title: "Plumbing & Sanitary System",
    description:
      "Complete water supply, drainage, and sanitary system installation for various building types.",
    badge: "Plumbing",
  },
  {
    icon: "i-lucide-building-2",
    title: "Civil & Architectural Works",
    description:
      "Commercial and industrial buildings, interior fit-outs, and retrofitting solutions.",
    badge: "Construction",
  },
  {
    icon: "i-lucide-shield",
    title: "Fire Protection System",
    description:
      "Design and installation of fire sprinkler and suppression systems for enhanced building safety.",
    badge: "Protection",
  },
  {
    icon: "i-lucide-calculator",
    title: "Project Estimation & Shop Drawings",
    description:
      "Accurate cost estimation and detailed shop drawings with or without sign and seal.",
    badge: "Engineering",
  },
];
</script>
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
