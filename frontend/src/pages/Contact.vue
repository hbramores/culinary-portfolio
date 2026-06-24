<script setup>
const contactCards = [
  {
    title: 'Email Address',
    value: 'hello@chefportfolio.com',
    icon: '✉️',
  },
  {
    title: 'Phone Number',
    value: '+63 917 123 4567',
    icon: '📞',
  },
  {
    title: 'Location',
    value: 'Manila, Philippines',
    icon: '📍',
  },
]

const socialLinks = [
  { name: 'Facebook', url: '#', icon: 'f' },
  { name: 'Instagram', url: '#', icon: 'i' },
  { name: 'TikTok', url: '#', icon: 't' },
  { name: 'LinkedIn', url: '#', icon: 'in' },
]
</script>

<template>
  <main class="bg-[#0D1B2A] text-[#F7F3E9]">
    <section class="relative overflow-hidden pt-24">
      <div class="absolute inset-0">
        <div class="absolute inset-0 bg-[url('../assets/images/atay-na-adobo.png')] bg-cover bg-center opacity-40" />
        <div class="absolute inset-0 bg-gradient-to-br from-[#0D1B2A]/85 via-[#0D1B2A]/70 to-[#0D1B2A]/95" />
      </div>
      <div class="relative mx-auto flex min-h-[55vh] max-w-6xl items-center px-6 py-24 sm:py-32">
        <div class="max-w-3xl space-y-6 text-center sm:text-left">
          <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Let's Connect</p>
          <h1 class="text-4xl font-semibold leading-tight text-[#F7F3E9] sm:text-5xl lg:text-6xl">
            Whether you're interested in my culinary journey, collaborations, or future opportunities, I'd love to hear from you.
          </h1>
          <p class="max-w-2xl text-base leading-8 text-[#F7F3E9]/80 sm:text-lg">
            Share your vision, collaboration ideas, or event requests and let's create something memorable together.
          </p>
        </div>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 py-16">
      <div class="mx-auto max-w-6xl px-6">
        <div class="grid gap-6 lg:grid-cols-[1.2fr_0.8fr]">
          <div class="space-y-6">
            <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Contact Information</p>
            <h2 class="text-3xl font-semibold text-[#F7F3E9] sm:text-4xl">Connect with the chef behind the portfolio.</h2>
            <p class="max-w-2xl text-base leading-8 text-[#F7F3E9]/80">
              As an aspiring chef and Hospitality Management student, I am passionate about creating memorable culinary experiences and continuously growing my skills in the culinary industry.
            </p>
            <div class="grid gap-4 sm:grid-cols-2">
              <article
                v-for="(card, index) in contactCards"
                :key="index"
                class="group rounded-[2rem] border border-white/10 bg-[#112339]/90 p-6 transition duration-300 hover:-translate-y-1 hover:border-[#D4AF37]/40"
              >
                <div class="inline-flex h-12 w-12 items-center justify-center rounded-3xl bg-[#D4AF37]/10 text-xl text-[#D4AF37] shadow-lg shadow-[#D4AF37]/10">
                  {{ card.icon }}
                </div>
                <p class="mt-6 text-sm uppercase tracking-[0.25em] text-[#D4AF37]/90">{{ card.title }}</p>
                <p class="mt-3 text-lg font-semibold text-[#F7F3E9]">{{ card.value }}</p>
              </article>
            </div>
          </div>

          <div class="rounded-[2rem] border border-white/10 bg-[#112339]/90 p-8 shadow-2xl shadow-black/20">
            <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Social Media</p>
            <h3 class="mt-4 text-2xl font-semibold text-[#F7F3E9]">Follow the chef’s culinary story.</h3>
            <div class="mt-8 grid gap-4">
              <a
                v-for="(social, index) in socialLinks"
                :key="index"
                :href="social.url"
                class="group flex items-center justify-between rounded-[1.75rem] border border-white/10 bg-[#0D1B2A]/90 px-6 py-5 text-[#F7F3E9] transition duration-300 hover:border-[#D4AF37]/40 hover:bg-[#142334]/90"
              >
                <span class="text-base font-medium">{{ social.name }}</span>
                <span class="inline-flex h-11 w-11 items-center justify-center rounded-full border border-[#F7F3E9]/10 bg-[#D4AF37]/10 text-sm text-[#D4AF37] transition duration-300 group-hover:bg-[#D4AF37] group-hover:text-[#0D1B2A]">
                  {{ social.icon }}
                </span>
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="border-t border-[#F7F3E9]/10 bg-[#0D1B2A] py-16">
      <div class="mx-auto max-w-6xl px-6">
        <div class="rounded-[2rem] border border-white/10 bg-[#112339]/90 p-10 shadow-2xl shadow-black/20 lg:flex lg:items-center lg:justify-between lg:gap-8">
          <div class="max-w-3xl">
            <p class="text-sm uppercase tracking-[0.3em] text-[#D4AF37]/90">Let's Create</p>
            <h2 class="mt-4 text-3xl font-semibold leading-tight text-[#F7F3E9] sm:text-4xl">Let's create something memorable together.</h2>
            <p class="mt-4 text-base leading-8 text-[#F7F3E9]/80">
              I’m always open to culinary collaborations, creative direction, and learning opportunities that bring fine dining Filipino cuisine to life.
            </p>
          </div>
          <div class="flex flex-col gap-4 sm:flex-row">
            <a
              href="mailto:hello@chefportfolio.com"
              class="inline-flex items-center justify-center rounded-full bg-[#D4AF37] px-8 py-4 text-sm font-semibold uppercase tracking-[0.2em] text-[#0D1B2A] transition duration-300 hover:bg-[#b38f2d]"
            >
              Send a Message
            </a>
            <RouterLink
              to="/menu"
              class="inline-flex items-center justify-center rounded-full border border-[#D4AF37] bg-transparent px-8 py-4 text-sm font-semibold uppercase tracking-[0.2em] text-[#F7F3E9] transition duration-300 hover:bg-[#D4AF37]/10"
            >
              View Culinary Portfolio
            </RouterLink>
          </div>
        </div>
      </div>
    </section>

    <footer class="border-t border-[#F7F3E9]/10 bg-[#09131f] py-10">
      <div class="mx-auto flex max-w-6xl flex-col gap-6 px-6 text-sm text-[#F7F3E9]/70 md:flex-row md:items-center md:justify-between">
        <p class="font-medium text-[#F7F3E9]">Chef Dwight Berja</p>
        <div class="flex flex-wrap items-center gap-4">
          <RouterLink to="/" class="transition duration-300 hover:text-[#D4AF37]">Home</RouterLink>
          <RouterLink to="/about" class="transition duration-300 hover:text-[#D4AF37]">About</RouterLink>
          <RouterLink to="/menu" class="transition duration-300 hover:text-[#D4AF37]">Menu</RouterLink>
          <RouterLink to="/contact" class="transition duration-300 hover:text-[#D4AF37]">Contact</RouterLink>
        </div>
        <p>© 2026 Chef Dwight Berja. All rights reserved.</p>
      </div>
    </footer>
  </main>
</template>