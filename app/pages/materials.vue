<script setup lang="ts">
interface MaterialGroup {
  title: string;
  description: string;
  items: string[];
}

const materialGroups: MaterialGroup[] = [
  {
    title: "Z - Zoom Construction Supply",
    description:
      "Construction supply line for core project requirements.",
    items: [
      "General construction materials",
      "Project-based supply support",
    ],
  },
  {
    title: "B - Booming Equipment Rental",
    description:
      "Equipment rental support for site and logistics operations.",
    items: [
      "Heavy equipment availability",
      "Project-based deployment and rental support",
    ],
  },
  {
    title: "N - Naturally Tech WPC PVC Panel Polycarbonates",
    description:
      "Panel and polycarbonate product line for architectural and finishing applications.",
    items: [
      "WPC materials",
      "PVC panels",
      "Polycarbonate sheets",
    ],
  },
  {
    title:
      "B - Boards-UP, Marine Plywood, Phenolic Board, Ordinary Plywood, Ficem Board, and Gypsum Board",
    description:
      "Board and plywood products for formworks, partitions, and interior construction.",
    items: [
      "Marine plywood",
      "Phenolic board",
      "Ordinary plywood",
      "Ficem board",
      "Gypsum board",
    ],
  },
  {
    title: "R - Revit Card Plotting and Drafting",
    description:
      "Drafting and plotting services for project and design documentation.",
    items: [
      "Revit drafting support",
      "Plan plotting services",
      "Technical drawing production",
    ],
  },
  {
    title: "Y - Y² Mechanical and Electrical Supplies",
    description:
      "Mechanical and electrical materials for installation and maintenance works.",
    items: [
      "Mechanical supplies",
      "Electrical supplies",
      "Project support items",
    ],
  },
  {
    title:
      "S - Steel de Sugbo (Roofing Sheets, Roll-Up Doors, Steel Deck, Plain Sheets, and Roofing Accessories)",
    description:
      "Steel and roofing product line for industrial and commercial envelope works.",
    items: [
      "Roofing sheets",
      "Roll-up doors",
      "Steel deck",
      "Plain sheets",
      "Roofing accessories",
    ],
  },
];
</script>

<template>
  <div>
    <section class="relative isolate overflow-hidden bg-zinc-950 text-white">
      <NuxtImg
        src="/images/IMG_2514.jpeg"
        alt="Construction materials and logistics"
        class="absolute inset-0 h-full w-full object-cover opacity-30"
        width="1800"
        height="1100"
      />
      <UContainer class="relative max-w-7xl mx-auto py-20">
        <div class="max-w-3xl space-y-4">
          <UBadge color="primary" variant="solid"> Material Supply </UBadge>
          <h1 class="font-heading text-4xl font-extrabold sm:text-5xl">
            Construction Materials and Product Supply
          </h1>
          <p class="text-zinc-200">
            Structured material sourcing aligned with project specifications,
            budget controls, and schedule requirements.
          </p>
        </div>
      </UContainer>
    </section>

    <section class="section-wrap">
      <UContainer class="max-w-7xl mx-auto space-y-6">
        <SectionTitle
          eyebrow="Product Handbook 2023"
          title="Core Material Categories"
          description="Catalog-style grouping to support estimating, procurement, and site implementation."
          align="center"
        />

        <div class="grid gap-6 md:grid-cols-2">
          <UCard
            v-for="group in materialGroups"
            :key="group.title"
            class="rounded-xl border border-zinc-200 shadow-xl"
          >
            <h3 class="font-heading text-xl font-bold text-zinc-950">
              {{ group.title }}
            </h3>
            <p class="mt-2 text-sm text-zinc-600">
              {{ group.description }}
            </p>
            <ul class="mt-4 space-y-2 text-sm text-zinc-700">
              <li
                v-for="item in group.items"
                :key="item"
                class="flex items-start gap-2"
              >
                <UIcon
                  name="i-lucide-check-circle-2"
                  class="mt-0.5 h-4 w-4 text-amber-500"
                />
                <span>{{ item }}</span>
              </li>
            </ul>
          </UCard>
        </div>
      </UContainer>
    </section>
  </div>
</template>
