<script setup>
import { computed, ref } from 'vue'
import heroImage from '@/assets/images/atay-na-adobo.png'
import pancitImage from '@/assets/images/pancit-canton-egg.png'

const categories = ['All', 'Main Course', 'Noodle Dishes', 'Desserts', 'Pastries', 'Beverages']
const activeCategory = ref('All')
const selectedDish = ref(null)

const dishes = [
  {
    id: 1,
    name: 'Crisp Adobo Mosaic',
    category: 'Main Course',
    description: 'A luxurious reinterpretation of adobo with caramelized soy, crisp shallots, and micro herbs.',
    time: '45 min',
    difficulty: 'Medium',
    skills: ['Filipino Cuisine', 'Plating', 'Food Preparation'],
    image: heroImage,
  },
  {
    id: 2,
    name: 'Silken Pancit Canton',
    category: 'Noodle Dishes',
    description: 'Hand-tossed egg noodles with seafood, garden vegetables, and calamansi finish.',
    time: '35 min',
    difficulty: 'Medium',
    skills: ['Knife Skills', 'Food Preparation', 'Filipino Cuisine'],
    image: pancitImage,
  },
  {
    id: 3,
    name: 'Golden Lechon Bites',
    category: 'Main Course',
    description: 'Luxury pork belly bites with citrus jus and delicate microgreen garnish.',
    time: '55 min',
    difficulty: 'Hard',
    skills: ['Plating', 'Food Safety', 'Menu Planning'],
    image: heroImage,
  },
  {
    id: 4,
    name: 'Coconut Panna Cotta',
    category: 'Desserts',
    description: 'Silky coconut cream finished with mango gel and toasted almond crumble.',
    time: '25 min',
    difficulty: 'Easy',
    skills: ['Baking', 'Plating', 'Food Preparation'],
    image: pancitImage,
  },
  {
    id: 5,
    name: 'Ube Brioche Slice',
    category: 'Pastries',
    description: 'Soft brioche infused with ube, accented by a gold dust glaze.',
    time: '70 min',
    difficulty: 'Medium',
    skills: ['Baking', 'Food Preparation', 'Menu Planning'],
    image: heroImage,
  },
  {
    id: 6,
    name: 'Calamansi Fizz',
    category: 'Beverages',
    description: 'Refreshing calamansi soda with ginger notes and a crisp citrus finish.',
    time: '10 min',
    difficulty: 'Easy',
    skills: ['Food Preparation', 'Menu Planning', 'Food Safety'],
    image: pancitImage,
  },
]

const filteredDishes = computed(() => {
  if (activeCategory.value === 'All') return dishes
  return dishes.filter((dish) => dish.category === activeCategory.value)
})

const featuredDishes = [
  {
    id: 101,
    name: 'Adobo Essence',
    category: 'Signature Dish',
    description: 'A premium tasting plate that balances heritage richness with elevated plating.',
    image: heroImage,
  },
  {
    id: 102,
    name: 'Pancit Canton Reverie',
    category: 'Signature Dish',
    description: 'A refined noodle composition with luxurious textures and modern Filipino elegance.',
    image: pancitImage,
  },
]

const openDish = (dish) => {
  selectedDish.value = dish
}

const closeDish = () => {
  selectedDish.value = null
}
</script>

<template>
  <main class="bg-[#0D1B2A] text-[#F7F3E9]">
    <section class="relative overflow-hidden pt-24">
      <div class="absolute inset-0">
        <img :src="heroImage" alt="Gourmet plated dish" class="h-full w-full object-cover object-center opacity-80" />
        <div class="absolute inset-0 bg-gradient-to-br from-[#0D1B2A]/85 via-[#0D1B2A]/70 to-[#0D1B2A]/95" />
      </div>
      <div class="relative mx-auto flex min-h-[60vh] max-w-6xl items-center px-6 py-28 sm:py-32">
        <div class="max-w-3xl space-y-6 text-center sm:text-left">
          <span class="inline-flex rounded-full border border-[#F7F3E9]/20 bg-[#F7F3E9]/5 px-4 py-2 text-xs uppercase tracking-[0.3em] text-[#F7F3E9]/80">
            Culinary Portfolio
          </span>
          <h1 class="text-4xl font-semibold leading-tight text-[#F7F3E9] sm:text-5xl lg:text-6xl">
            A collection of dishes showcasing passion, creativity, and culinary craftsmanship.
          </h1>
          <p class="max-w-2xl text-base leading-8 text-[#F7F3E9]/80 sm:text-lg">
            Explore each plated creation as a piece of culinary storytelling, designed for a refined fine dining experience.
          </p>
        </div>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 py-12">
      <div class="mx-auto max-w-6xl px-6">
        <div class="flex flex-wrap gap-3">
          <button
            v-for="category in categories"
            :key="category"
            type="button"
            @click="activeCategory = category"
            :class="['rounded-full border px-5 py-2 text-sm font-medium transition duration-300', activeCategory === category ? 'border-[#D4AF37] bg-[#D4AF37]/15 text-[#D4AF37]' : 'border-white/10 bg-[#112339]/90 text-[#F7F3E9]/80 hover:border-[#D4AF37]/40 hover:text-[#F7F3E9]']"
          >
            {{ category }}
          </button>
        </div>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 py-14">
      <div class="mx-auto max-w-6xl px-6">
        <div class="mb-10">
          <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Food Gallery</p>
          <h2 class="mt-4 text-3xl font-semibold text-[#F7F3E9] sm:text-4xl">Portfolio dishes with presentation first.</h2>
        </div>
        <div class="grid gap-8 md:grid-cols-2 xl:grid-cols-3">
          <article
            v-for="dish in filteredDishes"
            :key="dish.id"
            @click="openDish(dish)"
            class="group cursor-pointer overflow-hidden rounded-[2rem] border border-white/10 bg-[#112339]/90 shadow-2xl shadow-black/20 transition duration-500 hover:-translate-y-1 hover:border-[#D4AF37]/40"
          >
            <div class="relative h-72 overflow-hidden">
              <img :src="dish.image" :alt="dish.name" class="h-full w-full object-cover object-center transition duration-700 group-hover:scale-105" />
              <span class="absolute left-6 top-6 rounded-full border border-[#F7F3E9]/20 bg-[#0D1B2A]/80 px-4 py-2 text-xs uppercase tracking-[0.2em] text-[#D4AF37]">
                {{ dish.category }}
              </span>
            </div>
            <div class="space-y-4 p-6">
              <div>
                <h3 class="text-2xl font-semibold text-[#F7F3E9]">{{ dish.name }}</h3>
                <p class="mt-2 text-sm leading-7 text-[#F7F3E9]/80">{{ dish.description }}</p>
              </div>
              <div class="grid gap-3 sm:grid-cols-2">
                <div class="rounded-3xl bg-[#0E1A2B]/80 p-4 text-sm text-[#F7F3E9]/80">
                  <p class="uppercase tracking-[0.2em] text-[#D4AF37]/80">Prep Time</p>
                  <p class="mt-2 font-semibold text-[#F7F3E9]">{{ dish.time }}</p>
                </div>
                <div class="rounded-3xl bg-[#0E1A2B]/80 p-4 text-sm text-[#F7F3E9]/80">
                  <p class="uppercase tracking-[0.2em] text-[#D4AF37]/80">Difficulty</p>
                  <p class="mt-2 font-semibold text-[#F7F3E9]">{{ dish.difficulty }}</p>
                </div>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 bg-[#0D1B2A] py-14">
      <div class="mx-auto max-w-6xl px-6">
        <div class="mb-10">
          <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Featured Signature Dishes</p>
          <h2 class="mt-4 text-3xl font-semibold text-[#F7F3E9] sm:text-4xl">Elevated creations that define the chef’s portfolio.</h2>
        </div>
        <div class="grid gap-8 lg:grid-cols-2">
          <article
            v-for="dish in featuredDishes"
            :key="dish.id"
            class="overflow-hidden rounded-[2rem] border border-white/10 bg-[#112339]/90 shadow-[0_30px_80px_-50px_rgba(0,0,0,0.8)] transition duration-500 hover:-translate-y-1 hover:border-[#D4AF37]/40"
          >
            <div class="relative h-96 overflow-hidden">
              <img :src="dish.image" :alt="dish.name" class="h-full w-full object-cover object-center transition duration-700 group-hover:scale-105" />
              <div class="absolute inset-0 bg-gradient-to-t from-[#0D1B2A]/95 via-transparent to-transparent" />
            </div>
            <div class="space-y-4 p-10">
              <p class="text-xs uppercase tracking-[0.3em] text-[#D4AF37]/90">{{ dish.category }}</p>
              <h3 class="text-3xl font-semibold text-[#F7F3E9]">{{ dish.name }}</h3>
              <p class="text-base leading-8 text-[#F7F3E9]/80">{{ dish.description }}</p>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 py-16">
      <div class="mx-auto max-w-6xl px-6">
        <div class="rounded-[2rem] border border-white/10 bg-[#112339]/90 p-10 shadow-2xl shadow-black/20 lg:flex lg:items-center lg:justify-between lg:gap-8">
          <div class="max-w-3xl">
            <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Continue the story</p>
            <h2 class="mt-4 text-3xl font-semibold leading-tight text-[#F7F3E9] sm:text-4xl">Discover the chef’s journey and signature approach to modern Filipino fine dining.</h2>
          </div>
          <RouterLink
            to="/about"
            class="inline-flex items-center justify-center rounded-full bg-[#D4AF37] px-8 py-4 text-sm font-semibold uppercase tracking-[0.2em] text-[#0D1B2A] transition duration-300 hover:bg-[#b38f2d]"
          >
            Explore About
          </RouterLink>
        </div>
      </div>
    </section>

    <div v-if="selectedDish" class="fixed inset-0 z-50 bg-black/70 px-4 py-8 sm:px-6">
      <div class="mx-auto max-w-4xl overflow-hidden rounded-[2rem] border border-white/10 bg-[#0D1B2A] shadow-2xl shadow-black/50">
        <div class="relative h-96 overflow-hidden">
          <img :src="selectedDish.image" :alt="selectedDish.name" class="h-full w-full object-cover object-center" />
          <button
            @click="closeDish"
            class="absolute right-5 top-5 inline-flex h-11 w-11 items-center justify-center rounded-full border border-white/15 bg-[#0D1B2A]/80 text-[#F7F3E9] transition duration-300 hover:bg-[#D4AF37]/90 hover:text-[#0D1B2A]"
          >
            ✕
          </button>
        </div>
        <div class="space-y-6 p-8 sm:p-10">
          <div class="flex flex-col gap-3 sm:flex-row sm:items-center sm:justify-between">
            <div>
              <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">{{ selectedDish.category }}</p>
              <h2 class="mt-3 text-4xl font-semibold text-[#F7F3E9]">{{ selectedDish.name }}</h2>
            </div>
            <div class="grid gap-3 sm:grid-cols-2">
              <div class="rounded-3xl bg-[#112339]/90 p-4 text-sm text-[#F7F3E9]/80">
                <p class="uppercase tracking-[0.2em] text-[#D4AF37]/80">Prep Time</p>
                <p class="mt-2 font-semibold text-[#F7F3E9]">{{ selectedDish.time }}</p>
              </div>
              <div class="rounded-3xl bg-[#112339]/90 p-4 text-sm text-[#F7F3E9]/80">
                <p class="uppercase tracking-[0.2em] text-[#D4AF37]/80">Difficulty</p>
                <p class="mt-2 font-semibold text-[#F7F3E9]">{{ selectedDish.difficulty }}</p>
              </div>
            </div>
          </div>
          <p class="text-base leading-8 text-[#F7F3E9]/80">{{ selectedDish.description }}</p>
          <div class="rounded-[1.75rem] border border-[#F7F3E9]/10 bg-[#112339]/90 p-6">
            <p class="mb-4 text-sm uppercase tracking-[0.2em] text-[#D4AF37]/90">Culinary Skills Demonstrated</p>
            <div class="flex flex-wrap gap-3">
              <span v-for="(skill, index) in selectedDish.skills" :key="index" class="rounded-full border border-[#F7F3E9]/10 bg-[#0E1A2B]/90 px-4 py-2 text-sm text-[#F7F3E9]/80">
                {{ skill }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>