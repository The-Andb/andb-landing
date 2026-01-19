<script setup lang="ts">
import { useI18n } from 'vue-i18n'
import { Play } from 'lucide-vue-next'

const { t } = useI18n()
</script>

<template>
  <section id="demo" class="w-full max-w-5xl mx-auto mb-32 relative px-4 group perspective-container">
    <div class="text-center mb-16">
      <h2 class="text-3xl md:text-5xl font-black tracking-tight mb-4 text-white light-text-slate-900">{{ t('demo.title') }}</h2>
      <p class="text-xl text-slate-400 light-text-slate-600 max-w-2xl mx-auto">
        {{ t('demo.subtitle') }}
      </p>
    </div>

    <div class="relative bg-[#0f172a] rounded-[2rem] border border-slate-700/50 shadow-2xl overflow-hidden aspect-video transform transition-all hover:scale-[1.01] duration-500 group/video">
      <!-- Video Placeholder -->
      <div class="absolute inset-0 bg-slate-900/40 flex flex-col items-center justify-center gap-6">
        <div class="w-24 h-24 bg-indigo-500 rounded-full flex items-center justify-center shadow-2xl shadow-indigo-500/50 group-hover/video:scale-110 transition-transform cursor-pointer relative">
          <div class="absolute inset-0 bg-indigo-400 animate-ping rounded-full opacity-20"></div>
          <Play class="w-10 h-10 text-white fill-current ml-1 relative z-10" />
        </div>
        <div class="text-center">
          <span class="text-slate-400 font-mono text-sm uppercase tracking-widest bg-slate-900/80 px-6 py-2 rounded-full border border-white/5 backdrop-blur-md">
            demo_preview.mp4
          </span>
          <p class="mt-4 text-xs text-slate-500 italic">{{ t('demo.placeholder_note') }}</p>
        </div>
      </div>

      <!-- Overlay decoration -->
      <div class="absolute top-4 left-4 flex gap-2">
        <div class="w-3 h-3 rounded-full bg-red-500/20 border border-red-500/40"></div>
        <div class="w-3 h-3 rounded-full bg-yellow-500/20 border border-yellow-500/40"></div>
        <div class="w-3 h-3 rounded-full bg-green-500/20 border border-green-500/40"></div>
      </div>
    </div>
  </section>
</template>

<style scoped>
:global(body.light-mode) .light-text-slate-900 {
  @apply text-slate-900;
}
:global(body.light-mode) .light-text-slate-600 {
  @apply text-slate-600;
}
</style>
