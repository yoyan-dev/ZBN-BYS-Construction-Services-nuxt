<script setup lang="ts">
interface ProjectItem {
  title: string;
  category: string;
  description: string;
  image: string;
}

const projects: ProjectItem[] = [
  {
    title: "Westport Industrial Yard",
    category: "Industrial",
    description:
      "Multi-building manufacturing and storage yard with phased commissioning.",
    image: "/images/IMG_2521.jpeg",
  },
  {
    title: "Metroline Office Campus",
    category: "Commercial",
    description:
      "Corporate campus featuring smart access systems and energy-efficient facades.",
    image: "/images/IMG_2520.jpeg",
  },
  {
    title: "Harbor Freight Terminal",
    category: "Logistics",
    description:
      "Terminal expansion with reinforced pavements and high-capacity loading bays.",
    image: "/images/IMG_2518.jpeg",
  },
  {
    title: "Pioneer Energy Facility",
    category: "Energy",
    description:
      "Process area construction and control-room upgrade under strict safety requirements.",
    image: "/images/IMG_2517.jpeg",
  },
  {
    title: "Southlink Bridge Works",
    category: "Infrastructure",
    description:
      "Bridge rehabilitation and deck strengthening with managed traffic continuity.",
    image: "/images/IMG_2516.jpeg",
  },
  {
    title: "North District Utility Hub",
    category: "Civil",
    description:
      "Underground utility corridor and service hub enabling district redevelopment.",
    image: "/images/IMG_2515.jpeg",
  },
];
</script>
<template>
  <section class="section-wrap bg-zinc-50">
    <UContainer class="max-w-7xl mx-auto space-y-12">
      <SectionTitle
        eyebrow="Project Portfolio"
        title="Selected Projects"
        description="A selection of work delivered across complex and high-value construction environments."
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
</template>
