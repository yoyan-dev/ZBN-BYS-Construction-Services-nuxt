<script setup lang="ts">
interface EquipmentItem {
  name: string;
  capacity: string;
  description: string;
  image: string;
}

const equipment: EquipmentItem[] = [
  {
    name: "Mobile Crane",
    capacity: "Up to 50 tons",
    description:
      "Flexible lifting equipment for structural erection, plant support, and controlled heavy picks.",
    image: "/images/equipment/mobile-crane.jpg",
  },
  {
    name: "5 to 50 Tonner",
    capacity: "5T, 10T, 25T, 50T options",
    description:
      "Multi-capacity lifting lineup available for short-term and long-term project requirements.",
    image: "/images/equipment/5-to-50-tonner.jpg",
  },
  {
    name: "Boom Truck",
    capacity: "Hydraulic boom support",
    description:
      "Used for elevated lifting and transfer activities in tight or active project environments.",
    image: "/images/equipment/boom-truck.jpg",
  },
  {
    name: "Flat Truck",
    capacity: "General hauling",
    description:
      "Reliable transport for steel, formworks, pipe assemblies, and site-delivery materials.",
    image: "/images/equipment/flat-truck.jpg",
  },
  {
    name: "Back Hoe",
    capacity: "Digging and trenching",
    description:
      "Standard machine for excavation, backfilling, and utility trenching works.",
    image: "/images/equipment/back-hoe.jpg",
  },
  {
    name: "Dump Truck",
    capacity: "Bulk transport",
    description:
      "Used for hauling excavated soil, aggregates, debris, and base course materials.",
    image: "/images/equipment/dump-truck.jpg",
  },
  {
    name: "Ready Mix Concrete Truck",
    capacity: "Transit mixer delivery",
    description:
      "Concrete delivery support for foundations, slabs, columns, and structural pours.",
    image: "/images/equipment/ready-mix-concrete-truck.jpg",
  },
  {
    name: "Skid Loader",
    capacity: "Compact utility equipment",
    description:
      "Ideal for site clearing, palletized handling, and confined-area material movement.",
    image: "/images/equipment/skid-loader.jpg",
  },
  {
    name: "Loader",
    capacity: "High-volume loading",
    description:
      "Fast cycle machine for aggregate loading and high-volume transfer operations.",
    image: "/images/equipment/loader.jpg",
  },
  {
    name: "Compactor",
    capacity: "Ground and base compaction",
    description:
      "Supports road works, pad preparation, and density control before structural pours.",
    image: "/images/equipment/compactor.jpg",
  },
];
</script>

<template>
  <section class="section-wrap bg-zinc-50">
    <UContainer class="max-w-7xl mx-auto space-y-12">
      <SectionTitle
        eyebrow="Rental Equipment"
        title="Heavy Equipment and Machinery Rental"
        description="Available units for lifting, hauling, excavation, and concrete operations based on project demand."
        align="center"
      />

      <div class="grid gap-6 md:grid-cols-2 xl:grid-cols-3">
        <UCard
          v-for="item in equipment"
          :key="item.name"
          class="h-full overflow-hidden rounded-xl border border-zinc-200 shadow-xl"
        >
          <NuxtImg
            :src="item.image"
            :alt="item.name"
            class="h-56 w-full rounded-lg object-cover"
            width="1400"
            height="900"
            loading="lazy"
          />
          <div class="mt-5 space-y-3">
            <div class="flex items-center justify-between gap-3">
              <h3 class="font-heading text-lg font-bold text-zinc-950">
                {{ item.name }}
              </h3>
              <UBadge color="primary" variant="soft">
                {{ item.capacity }}
              </UBadge>
            </div>
            <p class="text-sm text-zinc-600">
              {{ item.description }}
            </p>
          </div>
        </UCard>
      </div>

      <UCard class="rounded-xl border border-zinc-200 shadow-xl">
        <h3 class="font-heading text-xl font-bold text-zinc-950">
          Rental Request Procedure
        </h3>
        <ul class="mt-4 space-y-2 text-sm text-zinc-600">
          <li>1. Send equipment type, quantity, and target schedule.</li>
          <li>2. Confirm site location, access condition, and work duration.</li>
          <li>3. Receive equipment availability and commercial quotation.</li>
          <li>4. Finalize mobilization and deployment schedule.</li>
        </ul>
      </UCard>
    </UContainer>
  </section>
</template>
