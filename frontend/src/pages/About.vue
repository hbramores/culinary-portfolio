<script setup>
const primarySkills = [
  'Food Preparation',
  'Knife Skills',
  'Plating & Presentation',
  'Baking',
  'Filipino Cuisine',
  'Food Safety',
  'Hospitality Service',
  'Menu Planning',
]

const educationTimeline = [
  {
    year: '2023',
    title: 'Hospitality Management Enrollment',
    description: 'Began formal studies in Hospitality Management with a focus on culinary operations and guest experience.',
  },
  {
    year: '2024',
    title: 'Culinary Training & Workshops',
    description: 'Completed hands-on culinary training in Filipino dishes, plating technique, and kitchen safety.',
  },
  {
    year: '2025',
    title: 'Fine Dining Mentorship',
    description: 'Refined skills in menu curation, service design, and elegant presentation through mentorship experiences.',
  },
]

const achievements = [
  {
    title: 'Signature Pop-Up Dinner',
    description: 'Curated a multi-course dining event highlighting modern Filipino flavors and premium plating.',
  },
  {
    title: 'Culinary Collaboration',
    description: 'Worked with local chefs to blend traditional recipes with contemporary fine dining styling.',
  },
  {
    title: 'Hospitality Showcase',
    description: 'Presented hospitality-driven culinary concepts to industry mentors and guests.',
  },
]
</script>

<template>
  <main class="bg-[#0D1B2A] text-[#F7F3E9]">
    <section class="relative overflow-hidden pt-24">
      <div class="absolute inset-0 bg-[radial-gradient(circle_at_top,_rgba(212,175,55,0.15),_transparent_30%),linear-gradient(180deg,_rgba(13,27,42,0.95),_rgba(13,27,42,0.95))]" />
      <div class="relative mx-auto flex min-h-[60vh] max-w-6xl items-center px-6 py-24 sm:py-32">
        <div class="grid gap-10 lg:grid-cols-[0.95fr_1.05fr] lg:items-center">
          <div class="space-y-6">
            <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">About the Chef</p>
            <h1 class="text-4xl font-semibold leading-tight text-[#F7F3E9] sm:text-5xl lg:text-6xl">A thoughtful modern chef building a premium culinary identity.</h1>
            <p class="max-w-3xl text-base leading-8 text-[#F7F3E9]/80 sm:text-lg">
              A Hospitality Management student with a passion for transforming Filipino heritage into elegant fine dining experiences. My story is a journey of growth, discipline, and culinary creativity.
            </p>
          </div>
          <div class="overflow-hidden rounded-[2rem] border border-white/10 bg-[#112339]/80 p-6 shadow-2xl shadow-black/20">
            <div class="aspect-video overflow-hidden rounded-[1.75rem] bg-[#0D1B2A]/80">
              <img src="../assets/images/pancit-canton-egg.png" alt="Chef portrait" class="h-full w-full object-cover object-center" />
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 py-16">
      <div class="mx-auto max-w-6xl px-6">
        <div class="grid gap-12 lg:grid-cols-[1.05fr_0.95fr] lg:items-center">
          <div class="space-y-6">
            <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">My Culinary Journey</p>
            <h2 class="text-3xl font-semibold text-[#F7F3E9] sm:text-4xl">A story of passion, learning, and creative growth.</h2>
            <p class="text-base leading-8 text-[#F7F3E9]/80">
              I find inspiration in Filipino flavors, hospitality culture, and the craft of plating food as a memorable visual and sensory moment. Each experience adds depth to the culinary story I am building.
            </p>
            <p class="text-base leading-8 text-[#F7F3E9]/80">
              From academic training to hands-on kitchen practice, my journey is guided by a desire to improve, innovate, and deliver refined dining experiences.
            </p>
          </div>
          <div class="overflow-hidden rounded-[2rem] border border-white/10 bg-[#112339]/90 p-6 shadow-2xl shadow-black/20">
            <div class="aspect-[4/5] overflow-hidden rounded-[1.75rem] bg-[#0D1B2A]/80">
              <img src="../assets/images/atay-na-adobo.png" alt="Culinary story image" class="h-full w-full object-cover object-center" />
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 py-16">
      <div class="mx-auto max-w-6xl px-6">
        <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Education</p>
        <h2 class="mt-4 text-3xl font-semibold text-[#F7F3E9] sm:text-4xl">Hospitality and culinary training built for a premium future.</h2>
        <div class="mt-10 space-y-6">
          <article
            v-for="(item, index) in educationTimeline"
            :key="index"
            class="rounded-[2rem] border border-white/10 bg-[#112339]/90 p-8 shadow-lg shadow-black/20"
          >
            <div class="flex flex-col gap-4 sm:flex-row sm:items-center sm:justify-between">
              <span class="rounded-full border border-[#D4AF37] bg-[#D4AF37]/10 px-5 py-3 text-sm uppercase tracking-[0.25em] text-[#D4AF37]">
                {{ item.year }}
              </span>
              <h3 class="text-2xl font-semibold text-[#F7F3E9]">{{ item.title }}</h3>
            </div>
            <p class="mt-4 text-base leading-8 text-[#F7F3E9]/80">{{ item.description }}</p>
          </article>
        </div>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 bg-[#0D1B2A] py-16">
      <div class="mx-auto max-w-6xl px-6 text-center">
        <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Culinary Philosophy</p>
        <h2 class="mt-4 text-3xl font-semibold text-[#F7F3E9] sm:text-4xl">Cooking is an act of thoughtful hospitality and memorable storytelling.</h2>
        <div class="mx-auto mt-10 max-w-3xl rounded-[2rem] border border-[#F7F3E9]/10 bg-[#112339]/90 p-10 text-left shadow-2xl shadow-black/20">
          <p class="text-xl leading-9 text-[#F7F3E9]/90 sm:text-2xl">
            “I believe every plate should invite guests into a story — one that reflects tradition, creativity, and the care put into every ingredient.”
          </p>
        </div>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 py-16">
      <div class="mx-auto max-w-6xl px-6">
        <div class="grid gap-10 lg:grid-cols-[0.65fr_0.35fr] lg:items-start">
          <div>
            <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Skills & Expertise</p>
            <h2 class="mt-4 text-3xl font-semibold text-[#F7F3E9] sm:text-4xl">A refined skillset built for culinary leadership.</h2>
            <div class="mt-8 grid gap-4 sm:grid-cols-2">
              <div
                v-for="(skill, index) in primarySkills"
                :key="index"
                class="rounded-[1.75rem] border border-white/10 bg-[#112339]/90 px-6 py-5 text-base text-[#F7F3E9]/80 transition duration-300 hover:-translate-y-1 hover:border-[#D4AF37]/40"
              >
                {{ skill }}
              </div>
            </div>
          </div>
          <div class="rounded-[2rem] border border-white/10 bg-[#112339]/90 p-8 shadow-2xl shadow-black/20">
            <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Looking Ahead</p>
            <h3 class="mt-4 text-3xl font-semibold text-[#F7F3E9]">Future chef career goals</h3>
            <ul class="mt-6 space-y-4 text-base leading-8 text-[#F7F3E9]/80">
              <li>Secure leadership opportunities in a premium culinary kitchen.</li>
              <li>Create modern Filipino tasting menus with refined presentation.</li>
              <li>Continue learning through mentorship, workshops, and international culinary exposure.</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 py-16">
      <div class="mx-auto max-w-6xl px-6">
        <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Featured Achievements</p>
        <h2 class="mt-4 text-3xl font-semibold text-[#F7F3E9] sm:text-4xl">Projects, collaborations, and culinary highlights.</h2>
        <div class="mt-10 grid gap-6 lg:grid-cols-3">
          <article
            v-for="(achievement, index) in achievements"
            :key="index"
            class="rounded-[2rem] border border-white/10 bg-[#112339]/90 p-8 shadow-lg shadow-black/20 transition duration-300 hover:-translate-y-1 hover:border-[#D4AF37]/40"
          >
            <h3 class="text-2xl font-semibold text-[#F7F3E9]">{{ achievement.title }}</h3>
            <p class="mt-4 text-base leading-8 text-[#F7F3E9]/80">{{ achievement.description }}</p>
          </article>
        </div>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 bg-[#0D1B2A] py-16">
      <div class="mx-auto max-w-6xl px-6">
        <div class="rounded-[2rem] border border-white/10 bg-[#112339]/90 p-10 shadow-2xl shadow-black/20 lg:flex lg:items-center lg:justify-between lg:gap-8">
          <div>
            <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Explore My Culinary Portfolio</p>
            <h2 class="mt-4 text-3xl font-semibold text-[#F7F3E9] sm:text-4xl">Experience the chef’s signature dishes and creative vision.</h2>
          </div>
          <div class="flex flex-col gap-4 sm:flex-row">
            <RouterLink
              to="/menu"
              class="inline-flex items-center justify-center rounded-full bg-[#D4AF37] px-8 py-4 text-sm font-semibold uppercase tracking-[0.2em] text-[#0D1B2A] transition duration-300 hover:bg-[#b38f2d]"
            >
              View Menu
            </RouterLink>
            <RouterLink
              to="/contact"
              class="inline-flex items-center justify-center rounded-full border border-[#D4AF37] bg-transparent px-8 py-4 text-sm font-semibold uppercase tracking-[0.2em] text-[#F7F3E9] transition duration-300 hover:bg-[#D4AF37]/10"
            >
              Contact Me
            </RouterLink>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>