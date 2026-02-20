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
    title: "Shop Drawing With/Without Sign and Seal",
    description:
      "Detailed drafting and technical plans with optional sign and seal support.",
    badge: "Engineering",
  },
  {
    icon: "i-lucide-calculator",
    title: "Project / Plan Estimation",
    description:
      "Cost estimation and planning support for project budgeting and scope control.",
    badge: "Pre-Construction",
  },
  {
    icon: "i-lucide-building-2",
    title: "Architectural Works",
    description:
      "Architectural scope execution from layout to finishing applications.",
    badge: "Construction",
  },
  {
    icon: "i-lucide-hard-hat",
    title: "Structural Works",
    description:
      "Structural construction services for reinforced and steel-based building systems.",
    badge: "Construction",
  },
  {
    icon: "i-lucide-zap",
    title: "Electrical Works (Commercial and Industrial Power System)",
    description:
      "Commercial and industrial electrical installations including distribution and controls.",
    badge: "Electrical",
  },
  {
    icon: "i-lucide-cpu",
    title: "Electronics",
    description:
      "Electronics systems integration for building operations and technical infrastructure.",
    badge: "ELV",
  },
  {
    icon: "i-lucide-droplets",
    title: "Plumbing System",
    description:
      "Water supply and piping network installation for residential, commercial, and industrial projects.",
    badge: "Plumbing",
  },
  {
    icon: "i-lucide-waves",
    title: "Sanitary System",
    description:
      "Sanitary layout and drainage system implementation with compliant installation methods.",
    badge: "Sanitary",
  },
  {
    icon: "i-lucide-wind",
    title:
      "HVAC SYSTEM (Ventilation System, Ducting System, Chilled Water System, AC System, VRF System)",
    description:
      "Complete HVAC works covering ventilation, ducting, chilled water, AC, and VRF systems.",
    badge: "Mechanical",
  },
  {
    icon: "i-lucide-shield-alert",
    title:
      "Fire Alarm System, Burglar System, CCTV Installation, Sanitary System, and Door Access",
    description:
      "Integrated life-safety and security systems including fire alarm, burglar, CCTV, sanitary interfaces, and door access.",
    badge: "Security",
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
