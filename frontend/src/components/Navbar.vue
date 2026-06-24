<script setup>
import { ref } from 'vue'

const isOpen = ref(false)

const toggleMenu = () => {
  isOpen.value = !isOpen.value
}
</script>

<template>
  <nav class="fixed inset-x-0 top-0 z-50 bg-[#0D1B2A]/20 backdrop-blur-2xl border-b border-[#F7F3E9]/12 shadow-[0_30px_80px_-40px_rgba(0,0,0,0.85)] text-[#F7F3E9]">
    <div class="max-w-7xl mx-auto px-6 py-4">

      <div class="flex items-center justify-between">
        <!-- Logo -->
        <RouterLink to="/" class="text-2xl font-semibold tracking-[0.22em] uppercase text-transparent bg-clip-text bg-gradient-to-r from-[#F7F3E9] via-[#D4AF37] to-[#F7F3E9]" @click="isOpen = false">
          Dwight Berja
        </RouterLink>

        <!-- Desktop Menu -->
        <ul class="hidden md:flex gap-8 text-sm font-medium">
          <li><RouterLink class="transition-colors duration-300 hover:text-[#D4AF37]" to="/" @click="isOpen = false">Home</RouterLink></li>
          <li><RouterLink class="transition-colors duration-300 hover:text-[#D4AF37]" to="/about" @click="isOpen = false">About</RouterLink></li>
          <li><RouterLink class="transition-colors duration-300 hover:text-[#D4AF37]" to="/menu" @click="isOpen = false">Menu</RouterLink></li>
          <li><RouterLink class="transition-colors duration-300 hover:text-[#D4AF37]" to="/contact" @click="isOpen = false">Contact</RouterLink></li>
        </ul>

        <!-- Hamburger Button -->
        <button
          @click="toggleMenu"
          class="md:hidden text-3xl text-[#F7F3E9] transition-colors duration-300 hover:text-[#D4AF37]"
          aria-label="Toggle navigation menu"
        >
          ☰
        </button>
      </div>

      <!-- Mobile Menu -->
      <div
        v-if="isOpen"
        class="md:hidden mt-4 rounded-3xl border border-white/10 bg-[#0D1B2A]/40 p-4 shadow-xl backdrop-blur-xl"
      >
        <ul class="flex flex-col gap-4 text-sm font-medium">
          <li><RouterLink class="block transition-colors duration-300 hover:text-[#D4AF37]" to="/" @click="isOpen = false">Home</RouterLink></li>
          <li><RouterLink class="block transition-colors duration-300 hover:text-[#D4AF37]" to="/about" @click="isOpen = false">About</RouterLink></li>
          <li><RouterLink class="block transition-colors duration-300 hover:text-[#D4AF37]" to="/menu" @click="isOpen = false">Menu</RouterLink></li>
          <li><RouterLink class="block transition-colors duration-300 hover:text-[#D4AF37]" to="/contact" @click="isOpen = false">Contact</RouterLink></li>
        </ul>
      </div>

    </div>
  </nav>
</template>