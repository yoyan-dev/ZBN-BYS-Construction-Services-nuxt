<script setup lang="ts">
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

interface CapabilityItem {
  icon: string;
  title: string;
  description: string;
}

interface MetricItem {
  value: string;
  label: string;
}

interface TrustIndicator {
  icon: string;
  value: string;
  description: string;
}

interface TestimonialItem {
  quote: string;
  name: string;
  role: string;
  company: string;
}

interface ContactItem {
  icon: string;
  label: string;
  value: string;
}

const heroMetrics: MetricItem[] = [
  {
    value: "18+",
    label: "Years of Experience",
  },
  {
    value: "320+",
    label: "Completed Projects",
  },
  {
    value: "24/7",
    label: "Project Coordination",
  },
];

const trustIndicators: TrustIndicator[] = [
  {
    icon: "i-lucide-briefcase-business",
    value: "18+ Years",
    description: "Serving commercial, industrial, and infrastructure sectors.",
  },
  {
    icon: "i-lucide-building-2",
    value: "320+ Projects",
    description: "Delivered with coordinated multidisciplinary execution.",
  },
  {
    icon: "i-lucide-badge-check",
    value: "Compliance-Ready",
    description: "Documentation support and code-aligned implementation.",
  },
];

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
    image: "/images/IMG_2520.jpeg",
  },
  {
    title: "Industrial Warehouse Development",
    category: "Industrial",
    description:
      "Design and build of an industrial warehouse including power distribution, ventilation systems, and sanitary works.",
    image: "/images/IMG_2517.jpeg",
  },
  {
    title: "Institutional Facility System Upgrade",
    category: "Infrastructure",
    description:
      "Retrofitting and system upgrade featuring fire detection, electrical improvements, and HVAC system enhancement.",
    image: "/images/IMG_2516.jpeg",
  },
];

const capabilities: CapabilityItem[] = [
  {
    icon: "i-lucide-drafting-compass",
    title: "Design & Build Expertise",
    description:
      "Integrated engineering and construction solutions from concept planning to project turnover.",
  },
  {
    icon: "i-lucide-shield-check",
    title: "Regulatory Assurance",
    description:
      "Complete documentation support and strict adherence to industry standards and authority requirements.",
  },
  {
    icon: "i-lucide-cpu",
    title: "Advanced Engineering",
    description:
      "Implementation of HVAC, electrical, fire protection, and plumbing systems using updated technologies.",
  },
  {
    icon: "i-lucide-handshake",
    title: "Collaborative Approach",
    description:
      "Close coordination with clients to balance functionality, efficiency, and cost-effectiveness.",
  },
];

const testimonials: TestimonialItem[] = [
  {
    quote:
      "The team was highly organized from planning to turnover. Reporting was clear and the final quality met our corporate standards.",
    name: "M. Santos",
    role: "Operations Head",
    company: "Harborline Logistics",
  },
  {
    quote:
      "Their multidisciplinary coordination helped us avoid delays during MEP integration. Communication stayed proactive throughout execution.",
    name: "J. Villanueva",
    role: "Project Director",
    company: "NorthGrid Developments",
  },
  {
    quote:
      "We valued their practical engineering input and compliance support. The project was delivered with strong safety discipline.",
    name: "R. Delgado",
    role: "Facilities Manager",
    company: "Westport Industrial Group",
  },
];

const contactItems: ContactItem[] = [
  {
    icon: "i-lucide-phone-call",
    label: "Call",
    value: "+639-489-1200",
  },
  {
    icon: "i-lucide-mail",
    label: "Email",
    value: "zbnbrysconstruction@gmail.com",
  },
  {
    icon: "i-lucide-map-pin",
    label: "Office",
    value: "Lapu Lapu City, Cebu Philippines",
  },
  {
    icon: "i-lucide-clock-3",
    label: "Response",
    value: "Within 24 to 48 hours",
  },
];
</script>

<template>
  <div class="overflow-hidden">
    <HeroSection
      title="Build with Confidence. Deliver with Precision."
      description="Design and build services for architectural, structural, mechanical, electrical, and electronics works delivered through disciplined project management."
      :metrics="heroMetrics"
    />

    <section class="relative z-10 -mt-12 pb-2">
      <UContainer class="section-shell">
        <div
          class="grid gap-4 rounded-2xl border border-slate-200 bg-white p-5 shadow-2xl md:grid-cols-3 md:p-7"
        >
          <div
            v-for="item in trustIndicators"
            :key="item.value"
            class="flex items-start gap-4 rounded-xl border border-slate-100 bg-slate-50/70 p-4"
          >
            <span
              class="grid h-11 w-11 shrink-0 place-items-center rounded-xl bg-brand-100 text-brand-700"
            >
              <UIcon :name="item.icon" class="h-5 w-5" />
            </span>
            <div class="space-y-1">
              <p class="font-heading text-lg font-bold text-slate-950">
                {{ item.value }}
              </p>
              <p class="text-sm text-slate-600">
                {{ item.description }}
              </p>
            </div>
          </div>
        </div>
      </UContainer>
    </section>

    <section class="section-wrap">
      <UContainer class="section-shell grid gap-10 lg:grid-cols-[1.1fr_0.9fr] lg:items-center">
        <div class="space-y-6">
          <SectionTitle
            eyebrow="About Us"
            title="A Trusted Construction Partner for Complex Builds"
            description="ZBN BRYS Construction Services handles technical execution across civil, architectural, mechanical, plumbing, and electrical disciplines."
          />

          <p class="text-slate-600">
            We support clients from planning through turnover with practical
            engineering alternatives, compliance-ready documentation, and
            structured project controls designed for schedule and cost certainty.
          </p>

          <div class="grid gap-3 sm:grid-cols-2">
            <div
              v-for="item in capabilities"
              :key="item.title"
              class="rounded-xl border border-slate-200 bg-white p-4"
            >
              <div class="flex items-start gap-3">
                <UIcon :name="item.icon" class="mt-0.5 h-5 w-5 text-brand-600" />
                <div>
                  <h3 class="font-heading text-base font-semibold text-slate-950">
                    {{ item.title }}
                  </h3>
                  <p class="mt-1 text-sm text-slate-600">
                    {{ item.description }}
                  </p>
                </div>
              </div>
            </div>
          </div>

          <div class="flex flex-wrap gap-3">
            <UButton size="lg" color="primary" to="/about">
              Explore Company Profile
            </UButton>
            <UButton size="lg" color="neutral" variant="outline" to="/contact">
              Request a Quote
            </UButton>
          </div>
        </div>

        <div class="grid gap-4 sm:grid-cols-2">
          <NuxtImg
            src="/images/IMG_2515.jpeg"
            alt="Construction management onsite coordination"
            class="h-full min-h-64 w-full rounded-2xl object-cover sm:col-span-2"
            width="1200"
            height="780"
            loading="lazy"
          />
          <NuxtImg
            src="/images/IMG_2521.jpeg"
            alt="Industrial project implementation"
            class="h-48 w-full rounded-2xl object-cover"
            width="900"
            height="640"
            loading="lazy"
          />
          <UCard class="rounded-2xl border border-brand-200 bg-brand-50 shadow-sm">
            <h3 class="font-heading text-xl font-bold text-brand-950">
              Certified-Ready Delivery
            </h3>
            <p class="mt-2 text-sm text-brand-900/85">
              We follow documented quality checks, safety protocols, and
              disciplined inspection workflows across all active sites.
            </p>
            <div class="mt-4 text-sm font-semibold text-brand-700">
              Quality, Safety, and Compliance First
            </div>
          </UCard>
        </div>
      </UContainer>
    </section>

    <section class="section-wrap bg-slate-50/90">
      <UContainer class="section-shell space-y-12">
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

        <div
          class="flex flex-col gap-4 rounded-2xl border border-brand-100 bg-white p-6 md:flex-row md:items-center md:justify-between"
        >
          <p class="text-slate-700">
            Need broader scope details? Review our specialized service coverage
            and technical capabilities.
          </p>
          <UButton size="lg" color="primary" to="/services">
            View All Services
          </UButton>
        </div>
      </UContainer>
    </section>

    <section class="section-wrap">
      <UContainer class="section-shell space-y-12">
        <SectionTitle
          eyebrow="Featured Work"
          title="Projects That Demonstrate Reliability"
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

        <div class="flex justify-center">
          <UButton size="lg" color="neutral" variant="outline" to="/projects">
            View Full Portfolio
          </UButton>
        </div>
      </UContainer>
    </section>

    <section class="section-wrap bg-brand-950 text-white">
      <UContainer class="section-shell space-y-12">
        <div class="space-y-5 text-center">
          <UBadge
            color="primary"
            variant="solid"
            class="rounded-full px-4 py-1.5 text-[11px] font-semibold uppercase tracking-[0.22em]"
          >
            Testimonials
          </UBadge>
          <h2 class="font-heading text-3xl font-extrabold sm:text-4xl">
            What Our Clients Say
          </h2>
          <p class="mx-auto max-w-3xl text-slate-200">
            We prioritize transparent communication, reliable execution, and
            measurable project outcomes that earn long-term client trust.
          </p>
        </div>

        <div class="grid gap-6 md:grid-cols-2 xl:grid-cols-3">
          <UCard
            v-for="item in testimonials"
            :key="item.name + item.company"
            class="rounded-2xl border border-white/12 bg-white/5 text-white shadow-xl backdrop-blur-sm"
          >
            <UIcon name="i-lucide-quote" class="h-6 w-6 text-brand-300" />
            <p class="mt-4 text-sm leading-relaxed text-slate-100">
              "{{ item.quote }}"
            </p>
            <div class="mt-6 border-t border-white/15 pt-4">
              <p class="font-heading text-base font-semibold text-white">
                {{ item.name }}
              </p>
              <p class="text-sm text-slate-300">
                {{ item.role }}, {{ item.company }}
              </p>
            </div>
          </UCard>
        </div>
      </UContainer>
    </section>

    <section class="section-wrap">
      <UContainer class="section-shell">
        <div class="grid gap-8 lg:grid-cols-[1.25fr_0.75fr]">
          <UCard class="rounded-2xl border border-slate-200 bg-white shadow-xl">
            <SectionTitle
              eyebrow="Contact Section"
              title="Start Your Project with a Free Estimate"
              description="Share your project scope, target schedule, and technical requirements. Our team will prepare a tailored proposal."
            />

            <div class="mt-8 grid gap-4 sm:grid-cols-2">
              <div
                v-for="item in contactItems"
                :key="item.label"
                class="rounded-xl border border-slate-200 bg-slate-50/80 p-4"
              >
                <div class="flex items-start gap-3">
                  <UIcon :name="item.icon" class="mt-0.5 h-5 w-5 text-brand-600" />
                  <div>
                    <p class="text-xs font-semibold uppercase tracking-[0.12em] text-slate-500">
                      {{ item.label }}
                    </p>
                    <p class="text-sm font-medium text-slate-800">
                      {{ item.value }}
                    </p>
                  </div>
                </div>
              </div>
            </div>

            <div class="mt-8 flex flex-wrap gap-3">
              <UButton size="lg" color="primary" to="/contact">
                Get a Free Estimate
              </UButton>
              <UButton size="lg" color="neutral" variant="outline" to="/services">
                Review Service Coverage
              </UButton>
            </div>
          </UCard>

          <UCard class="rounded-2xl border border-brand-200 bg-brand-50 shadow-sm">
            <h3 class="font-heading text-2xl font-bold text-brand-950">
              Why Clients Move Fast with Us
            </h3>
            <ul class="mt-5 space-y-4 text-sm text-brand-900/85">
              <li class="flex items-start gap-3">
                <UIcon
                  name="i-lucide-check-circle-2"
                  class="mt-0.5 h-5 w-5 text-brand-600"
                />
                Scope-aligned planning before execution begins
              </li>
              <li class="flex items-start gap-3">
                <UIcon
                  name="i-lucide-check-circle-2"
                  class="mt-0.5 h-5 w-5 text-brand-600"
                />
                Practical cost control and milestone tracking
              </li>
              <li class="flex items-start gap-3">
                <UIcon
                  name="i-lucide-check-circle-2"
                  class="mt-0.5 h-5 w-5 text-brand-600"
                />
                Dedicated technical support from concept to turnover
              </li>
            </ul>
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
