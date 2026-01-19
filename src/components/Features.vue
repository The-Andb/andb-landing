<script setup lang="ts">
import { ref } from 'vue'
import { ChevronLeft, ChevronRight } from 'lucide-vue-next'

const activeIndex = ref(1) // Start at center
const slides = [
  { img: '/screenshots/dashboard.png', label: 'Project Dashboard' },
  { img: '/screenshots/compare-detail.png', label: 'Visual Schema Compare' },
  { img: '/screenshots/schema.png', label: 'Interactive ER Diagram' },
  { img: '/screenshots/history.png', label: 'Migration History' },
  { img: '/screenshots/settings.png', label: 'Settings & Config' }
]

const next = () => activeIndex.value = (activeIndex.value + 1) % slides.length
const prev = () => activeIndex.value = (activeIndex.value - 1 + slides.length) % slides.length
</script>

<template>
  <div class="relative w-full mx-auto mt-20 perspective-container h-[600px] flex items-center justify-center overflow-visible">
    
    <!-- Controls -->
    <button @click="prev" class="absolute left-4 md:left-10 z-50 p-4 rounded-full bg-slate-800/80 border border-white/10 hover:bg-white/10 transition-colors backdrop-blur-md">
      <ChevronLeft class="w-8 h-8 text-white" />
    </button>
    <button @click="next" class="absolute right-4 md:right-10 z-50 p-4 rounded-full bg-slate-800/80 border border-white/10 hover:bg-white/10 transition-colors backdrop-blur-md">
      <ChevronRight class="w-8 h-8 text-white" />
    </button>

    <!-- Carousel Track -->
    <div class="relative w-full h-full flex items-center justify-center transform-style-3d">
       <div v-for="(slide, index) in slides" :key="index"
            class="absolute transition-all duration-700 ease-[cubic-bezier(0.25,0.8,0.25,1)] cursor-pointer rounded-2xl overflow-hidden shadow-2xl border border-white/10"
            :class="{
              'z-30 scale-100 opacity-100 translate-x-0': index === activeIndex,
              'z-10 scale-[0.85] opacity-40 -translate-x-[65%] rotate-y-12 blur-[2px] hover:opacity-80 hover:blur-0': index === (activeIndex + 1) % slides.length,
              'z-10 scale-[0.85] opacity-40 translate-x-[65%] -rotate-y-12 blur-[2px] hover:opacity-80 hover:blur-0': index === (activeIndex - 1 + slides.length) % slides.length,
              'z-0 scale-50 opacity-0': Math.abs(index - activeIndex) > 1 && !(index === 0 && activeIndex === slides.length - 1) && !(index === slides.length - 1 && activeIndex === 0)
            }"
            @click="activeIndex = index"
            >
          <!-- Image -->
          <img :src="slide.img" class="w-[85vw] md:w-[1000px] h-auto object-contain bg-slate-900" alt="Screenshot" />
          <div class="absolute bottom-0 w-full bg-gradient-to-t from-black/90 to-transparent p-6 pt-20 text-center">
            <h3 class="text-white font-bold text-xl md:text-2xl">{{ slide.label }}</h3>
          </div>
       </div>
    </div>

  </div>
</template>

<style scoped>
.perspective-container {
  perspective: 2000px;
}
.rotate-y-12 {
  transform: translateX(65%) scale(0.85) rotateY(-35deg);
}
.-rotate-y-12 {
  transform: translateX(-65%) scale(0.85) rotateY(35deg);
}
</style>
