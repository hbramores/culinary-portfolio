<script setup>
import heroImage from '@/assets/images/atay-na-adobo.png'
import pancitImage from '@/assets/images/pancit-canton-egg.png'

const creations = [
  {
    title: 'Slow-Braised Adobo',
    category: 'Signature Dish',
    description: 'A refined adobo with soy-caramel depth, crispy shallots, and modern plating.',
    image: heroImage,
  },
  {
    title: 'Pancit Canton Elegance',
    category: 'Heritage Favorite',
    description: 'Premium egg noodles paired with seafood, crisp vegetables, and calamansi bright notes.',
    image: pancitImage,
  },
  {
    title: 'Golden Lechon Kawali',
    category: 'Fine Dining Twist',
    description: 'Crispy pork belly bites finished with citrus jus, microgreens, and luxurious texture.',
    image: heroImage,
  },
]

const skills = [
  'Knife Skills',
  'Food Preparation',
  'Plating',
  'Baking',
  'Filipino Cuisine',
  'Food Safety',
  'Menu Planning',
]

const journey = [
  {
    year: '2024',
    title: 'Hospitality Management Student',
    details: 'Studying hospitality with a focus on culinary operations, service design, and kitchen leadership.',
  },
  {
    year: '2025',
    title: 'Professional Culinary Training',
    details: 'Completed hands-on training in modern Filipino cuisine, fine dining techniques, and menu curation.',
  },
  {
    year: '2026',
    title: 'Aspiring Executive Chef',
    details: 'Moving toward a professional kitchen role with a dedication to elegant storytelling through food.',
  },
]
</script>

<template>
  <main class="bg-[#0D1B2A] text-[#F7F3E9]">
    <section class="relative min-h-screen overflow-hidden pt-24">
      <div class="absolute inset-0">
        <img
          :src="heroImage"
          alt="Featured chef dish"
          class="h-full w-full object-cover object-center opacity-70"
        />
        <div class="absolute inset-0 bg-gradient-to-b from-black/20 via-[#0D1B2A]/70 to-[#0D1B2A]/95"></div>
      </div>

      <div class="relative z-10 mx-auto flex min-h-[calc(100vh-6rem)] max-w-6xl items-center px-6 py-20">
        <div class="space-y-8 text-center sm:text-left">
          <span class="inline-flex rounded-full border border-[#F7F3E9]/20 bg-[#F7F3E9]/5 px-4 py-2 text-xs uppercase tracking-[0.3em] text-[#F7F3E9]/80">
            Filipino chef portfolio
          </span>
          <h1 class="text-4xl font-semibold leading-tight text-[#F7F3E9] sm:text-6xl lg:text-7xl">
            Chef Dwight Berja
          </h1>
          <p class="mx-auto max-w-3xl text-base leading-8 text-[#F7F3E9]/90 sm:mx-0 sm:text-lg">
            Crafting memorable culinary experiences through passion and creativity.
          </p>
          <div class="mx-auto flex flex-col items-center justify-center gap-4 pt-4 sm:mx-0 sm:flex-row">
            <RouterLink
              to="/creations"
              class="inline-flex items-center justify-center rounded-full bg-[#D4AF37] px-8 py-3 text-sm font-semibold uppercase tracking-[0.2em] text-[#0D1B2A] shadow-[0_20px_60px_-30px_rgba(212,175,55,0.9)] transition duration-300 hover:-translate-y-0.5 hover:bg-[#b38f2d]"
            >
              View Creations
            </RouterLink>
            <a
              href="#about"
              class="inline-flex items-center justify-center rounded-full border border-[#F7F3E9]/20 bg-white/5 px-8 py-3 text-sm font-medium text-[#F7F3E9] transition duration-300 hover:border-[#D4AF37] hover:text-[#D4AF37]"
            >
              Meet the Chef
            </a>
          </div>
        </div>
      </div>
    </section>

    <section id="about" class="border-t border-[#F7F3E9]/10 bg-[#0D1B2A] py-20">
      <div class="mx-auto grid max-w-6xl gap-12 px-6 lg:grid-cols-[1.05fr_0.95fr] lg:items-center">
        <div class="overflow-hidden rounded-[2rem] border border-white/10 bg-[#152139]/80 shadow-2xl shadow-black/20">
          <img
            :src="pancitImage"
            alt="Chef portrait with premium plating"
            class="h-full w-full object-cover object-center"
          />
        </div>

        <div class="space-y-6">
          <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">About</p>
          <h2 class="text-3xl font-semibold text-[#F7F3E9] sm:text-4xl">Hospitality-driven chef crafting elevated Filipino cuisine.</h2>
          <p class="max-w-xl text-base leading-8 text-[#F7F3E9]/80">
            I am a Hospitality Management student with a steadfast aspiration to become a professional chef. Every plate I create is rooted in discipline, cultural pride, and modern fine dining presentation.
          </p>
          <div class="grid gap-4 sm:grid-cols-2">
            <div class="rounded-3xl border border-[#F7F3E9]/10 bg-[#142333]/75 p-6 shadow-lg shadow-black/20">
              <p class="mb-2 text-sm uppercase tracking-[0.2em] text-[#D4AF37]/85">Experience</p>
              <p class="text-sm leading-7 text-[#F7F3E9]/80">Culinary training in contemporary Filipino dishes and hospitality operations.</p>
            </div>
            <div class="rounded-3xl border border-[#F7F3E9]/10 bg-[#142333]/75 p-6 shadow-lg shadow-black/20">
              <p class="mb-2 text-sm uppercase tracking-[0.2em] text-[#D4AF37]/85">Approach</p>
              <p class="text-sm leading-7 text-[#F7F3E9]/80">Elegant plating, meticulous technique, and a premium dining narrative on every plate.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 py-20">
      <div class="mx-auto max-w-6xl px-6">
        <div class="mb-12 max-w-2xl">
          <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Featured Creations</p>
          <h2 class="mt-4 text-3xl font-semibold text-[#F7F3E9] sm:text-4xl">Signature dishes with refined Filipino soul.</h2>
          <p class="mt-4 text-base leading-8 text-[#F7F3E9]/80">A curated selection of plated creations designed for discerning guests and memorable tasting experiences.</p>
        </div>

        <div class="grid gap-8 md:grid-cols-3">
          <article
            v-for="(dish, index) in creations"
            :key="index"
            class="group overflow-hidden rounded-[2rem] border border-white/10 bg-[#112339]/90 shadow-[0_30px_80px_-50px_rgba(0,0,0,0.8)] transition duration-500 hover:-translate-y-1 hover:border-[#D4AF37]/40"
          >
            <div class="relative h-72 overflow-hidden">
              <img
                :src="dish.image"
                :alt="dish.title"
                class="h-full w-full object-cover object-center transition duration-700 group-hover:scale-105"
              />
              <div class="absolute inset-x-0 bottom-0 rounded-t-[2rem] bg-gradient-to-t from-[#0D1B2A]/95 via-transparent to-transparent p-6 text-[#F7F3E9]">
                <p class="text-xs uppercase tracking-[0.2em] text-[#D4AF37]">{{ dish.category }}</p>
                <h3 class="mt-3 text-2xl font-semibold">{{ dish.title }}</h3>
              </div>
            </div>
            <div class="space-y-4 p-6">
              <p class="text-sm leading-7 text-[#F7F3E9]/80">{{ dish.description }}</p>
              <div class="flex items-center gap-2 text-xs uppercase tracking-[0.25em] text-[#D4AF37]/90">
                <span class="inline-flex h-2 w-2 rounded-full bg-[#D4AF37]" />
                <span>Fine dining plating</span>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 bg-[#0D1B2A] py-20">
      <div class="mx-auto max-w-6xl px-6">
        <div class="mb-12 max-w-2xl">
          <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Culinary Skills</p>
          <h2 class="mt-4 text-3xl font-semibold text-[#F7F3E9] sm:text-4xl">Refined skills for every service.</h2>
        </div>

        <div class="grid gap-4 sm:grid-cols-2 lg:grid-cols-3">
          <div v-for="(skill, index) in skills" :key="index" class="rounded-3xl border border-[#F7F3E9]/10 bg-[#112339]/80 p-5 text-center shadow-lg shadow-black/20 transition duration-300 hover:-translate-y-1 hover:border-[#D4AF37]/40">
            <p class="text-base font-semibold text-[#F7F3E9]">{{ skill }}</p>
          </div>
        </div>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 py-20">
      <div class="mx-auto max-w-6xl px-6">
        <div class="grid gap-10 lg:grid-cols-[0.4fr_0.6fr]">
          <div class="flex items-center">
            <div class="space-y-6">
              <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Culinary Journey</p>
              <h2 class="text-3xl font-semibold text-[#F7F3E9] sm:text-4xl">A modern trajectory from training to chef leadership.</h2>
            </div>
          </div>

          <div class="relative">
            <div class="absolute left-5 top-2 h-full w-px bg-[#F7F3E9]/20"></div>
            <div class="space-y-10 pl-10">
              <article v-for="(step, index) in journey" :key="index" class="relative">
                <div class="absolute left-[-0.5rem] top-2 flex h-10 w-10 items-center justify-center rounded-full border border-[#D4AF37] bg-[#D4AF37]/10 text-[#D4AF37] shadow-xl shadow-[#D4AF37]/10">
                  {{ step.year }}
                </div>
                <div class="rounded-3xl border border-[#F7F3E9]/10 bg-[#13203a]/90 p-8 shadow-lg shadow-black/20">
                  <p class="text-sm uppercase tracking-[0.25em] text-[#D4AF37]/90">{{ step.title }}</p>
                  <p class="mt-4 text-base leading-7 text-[#F7F3E9]/80">{{ step.details }}</p>
                </div>
              </article>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 bg-[#121d31] py-20">
      <div class="mx-auto max-w-5xl px-6 text-center">
        <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Quote</p>
        <h2 class="mt-6 text-4xl font-semibold leading-tight text-[#F7F3E9] sm:text-5xl">
          “Every dish should feel like an invitation to savor a carefully curated moment.”
        </h2>
        <p class="mt-6 text-base leading-8 text-[#F7F3E9]/75">Elegant cuisine is built from discipline, thoughtful technique, and the quiet confidence to let every ingredient shine.</p>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 py-20">
      <div class="mx-auto max-w-6xl px-6">
        <div class="grid gap-8 rounded-[2rem] border border-[#F7F3E9]/10 bg-[#112339]/90 p-10 shadow-2xl shadow-black/20 lg:grid-cols-[1.3fr_0.7fr] lg:items-center">
          <div>
            <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Contact</p>
            <h2 class="mt-4 text-3xl font-semibold text-[#F7F3E9] sm:text-4xl">Ready to collaborate on an exceptional dining experience?</h2>
            <p class="mt-4 max-w-xl text-base leading-8 text-[#F7F3E9]/80">Let's connect about catering, restaurant projects, or culinary concept development with a modern Filipino fine dining vision.</p>
          </div>
          <div class="space-y-4 text-center">
            <RouterLink
              to="/contact"
              class="inline-flex w-full items-center justify-center rounded-full bg-[#D4AF37] px-8 py-4 text-sm font-semibold uppercase tracking-[0.2em] text-[#0D1B2A] transition duration-300 hover:bg-[#b38f2d]"
            >
              Contact the Chef
            </RouterLink>
            <div class="flex flex-wrap justify-center gap-4 text-[#F7F3E9]/80">
              <a href="#" class="transition duration-300 hover:text-[#D4AF37]">Instagram</a>
              <a href="#" class="transition duration-300 hover:text-[#D4AF37]">LinkedIn</a>
              <a href="#" class="transition duration-300 hover:text-[#D4AF37]">Email</a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <footer class="border-t border-[#F7F3E9]/10 bg-[#09131f] py-10">
      <div class="mx-auto flex max-w-6xl flex-col gap-6 px-6 text-sm text-[#F7F3E9]/70 md:flex-row md:items-center md:justify-between">
        <p class="font-medium text-[#F7F3E9]">Chef Dwight Berja</p>
        <div class="flex flex-wrap items-center gap-4">
          <a href="/" class="transition duration-300 hover:text-[#D4AF37]">Home</a>
          <a href="/about" class="transition duration-300 hover:text-[#D4AF37]">About</a>
          <a href="/creations" class="transition duration-300 hover:text-[#D4AF37]">Creations</a>
          <a href="/contact" class="transition duration-300 hover:text-[#D4AF37]">Contact</a>
        </div>
        <p>© 2026 Dwight Berja. All rights reserved.</p>
      </div>
    </footer>
  </main>
</template>