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

<script setup lang="ts">
interface ProjectItem {
  title: string
  category: string
  description: string
  image: string
}

const projects: ProjectItem[] = [
  {
    title: 'Westport Industrial Yard',
    category: 'Industrial',
    description: 'Multi-building manufacturing and storage yard with phased commissioning.',
    image: 'https://images.unsplash.com/photo-1599707367072-cd6ada2bc375?auto=format&fit=crop&w=1200&q=80'
  },
  {
    title: 'Metroline Office Campus',
    category: 'Commercial',
    description: 'Corporate campus featuring smart access systems and energy-efficient facades.',
    image: 'https://images.unsplash.com/photo-1489515217757-5fd1be406fef?auto=format&fit=crop&w=1200&q=80'
  },
  {
    title: 'Harbor Freight Terminal',
    category: 'Logistics',
    description: 'Terminal expansion with reinforced pavements and high-capacity loading bays.',
    image: 'https://images.unsplash.com/photo-1479839672679-a46483c0e7c8?auto=format&fit=crop&w=1200&q=80'
  },
  {
    title: 'Pioneer Energy Facility',
    category: 'Energy',
    description: 'Process area construction and control-room upgrade under strict safety requirements.',
    image: 'https://images.unsplash.com/photo-1469474968028-56623f02e42e?auto=format&fit=crop&w=1200&q=80'
  },
  {
    title: 'Southlink Bridge Works',
    category: 'Infrastructure',
    description: 'Bridge rehabilitation and deck strengthening with managed traffic continuity.',
    image: 'https://images.unsplash.com/photo-1517581177682-a085bb7ffb15?auto=format&fit=crop&w=1200&q=80'
  },
  {
    title: 'North District Utility Hub',
    category: 'Civil',
    description: 'Underground utility corridor and service hub enabling district redevelopment.',
    image: 'https://images.unsplash.com/photo-1505843513577-22bb7d21e455?auto=format&fit=crop&w=1200&q=80'
  }
]
</script>
