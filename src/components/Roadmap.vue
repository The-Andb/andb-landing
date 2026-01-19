<script setup lang="ts">
import { useI18n } from 'vue-i18n'
import { CheckCircle, Loader, ShieldCheck, Database, LayoutTemplate } from 'lucide-vue-next'

const { t } = useI18n()
</script>

<template>
  <section id="roadmap" class="max-w-7xl mx-auto px-6 py-32 relative">
    <div class="text-center mb-20">
      <div class="inline-flex items-center px-4 py-1.5 rounded-full border border-indigo-500/30 bg-indigo-500/10 text-indigo-300 text-sm font-medium backdrop-blur-md mb-6">
        <span class="flex h-2.5 w-2.5 rounded-full bg-indigo-400 mr-2.5 animate-pulse"></span>
        {{ t('roadmap.vision_badge') }}
      </div>
      <h2 class="text-4xl md:text-6xl font-black tracking-tight mb-6">{{ t('roadmap.title') }}</h2>
      <p class="text-xl text-slate-400 light-text-slate-600 max-w-3xl mx-auto">
        {{ t('roadmap.subtitle') }}
      </p>
    </div>

    <!-- Timeline Grid -->
    <div class="grid grid-cols-1 lg:grid-cols-4 gap-6 mb-20">
      <!-- Phase 1 -->
      <div class="glass-card p-6 rounded-2xl border-green-500/20 relative group hover:-translate-y-1 transition-transform duration-300">
        <div class="absolute top-4 right-4 text-green-500">
          <CheckCircle class="w-5 h-5" />
        </div>
        <div class="text-xs font-mono text-green-400 font-bold uppercase tracking-wider mb-2">Phase 1</div>
        <h3 class="text-lg font-bold text-white light-text-slate-900 mb-2">{{ t('roadmap.phase1.title') }}</h3>
        <p class="text-slate-400 light-text-slate-600 text-sm mb-4">{{ t('roadmap.phase1.desc') }}</p>
        <div class="inline-block px-2 py-1 rounded bg-green-500/10 text-green-400 text-[10px] font-bold">{{ t('roadmap.status_live') }}</div>
      </div>

      <!-- Phase 2 (Active) -->
      <div class="glass-card p-6 rounded-2xl border-indigo-500/50 bg-indigo-500/5 relative group ring-1 ring-indigo-500/30 hover:-translate-y-1 transition-transform duration-300">
        <div class="absolute top-4 right-4 text-indigo-400 animate-spin-slow">
          <Loader class="w-5 h-5" />
        </div>
        <div class="text-xs font-mono text-indigo-300 font-bold uppercase tracking-wider mb-2">Phase 2</div>
        <h3 class="text-lg font-bold text-white light-text-slate-900 mb-2">{{ t('roadmap.phase2.title') }}</h3>
        <p class="text-slate-400 light-text-slate-600 text-sm mb-4">{{ t('roadmap.phase2.desc') }}</p>
        <div class="inline-block px-2 py-1 rounded bg-indigo-500/20 text-indigo-300 text-[10px] font-bold">{{ t('roadmap.phase2.date') }}</div>
      </div>

      <!-- Phase 3 -->
      <div class="glass-card p-6 rounded-2xl border-white/5 relative group opacity-80 hover:opacity-100 hover:-translate-y-1 transition-all duration-300">
        <div class="text-xs font-mono text-slate-500 font-bold uppercase tracking-wider mb-2">Phase 3</div>
        <h3 class="text-lg font-bold text-white light-text-slate-900 mb-2">{{ t('roadmap.phase3.title') }}</h3>
        <p class="text-slate-400 light-text-slate-600 text-sm mb-4">{{ t('roadmap.phase3.desc') }}</p>
        <div class="inline-block px-2 py-1 rounded bg-slate-800 text-slate-400 text-[10px] font-bold">{{ t('roadmap.phase3.date') }}</div>
      </div>

      <!-- Phase 4 -->
      <div class="glass-card p-6 rounded-2xl border-white/5 relative group opacity-60 hover:opacity-100 hover:-translate-y-1 transition-all duration-300">
        <div class="text-xs font-mono text-slate-500 font-bold uppercase tracking-wider mb-2">Phase 4</div>
        <h3 class="text-lg font-bold text-white light-text-slate-900 mb-2">{{ t('roadmap.phase4.title') }}</h3>
        <p class="text-slate-400 light-text-slate-600 text-sm mb-4">{{ t('roadmap.phase4.desc') }}</p>
        <div class="inline-block px-2 py-1 rounded bg-slate-800 text-slate-400 text-[10px] font-bold">{{ t('roadmap.phase4.date') }}</div>
      </div>
    </div>

    <!-- Details Grid -->
    <div class="grid lg:grid-cols-2 gap-12">
      <!-- Active Focus -->
      <div>
        <h3 class="text-2xl font-bold text-white light-text-slate-900 mb-8 flex items-center gap-3">
          <span class="w-2 h-2 rounded-full bg-indigo-500 animate-pulse"></span>
          {{ t('roadmap.focus_title') }}
        </h3>
        
        <div class="space-y-6">
          <div class="flex gap-4 group">
            <div class="shrink-0 w-12 h-12 rounded-xl bg-indigo-500/10 flex items-center justify-center text-indigo-400 group-hover:scale-110 transition-transform">
              <Database class="w-6 h-6" />
            </div>
            <div>
              <h4 class="text-white light-text-slate-900 font-bold mb-1 text-lg">{{ t('roadmap.focus.pg_title') }}</h4>
              <p class="text-slate-400 light-text-slate-600 text-sm leading-relaxed">
                {{ t('roadmap.focus.pg_desc') }}
              </p>
            </div>
          </div>

          <div class="flex gap-4 group">
             <div class="shrink-0 w-12 h-12 rounded-xl bg-purple-500/10 flex items-center justify-center text-purple-400 group-hover:scale-110 transition-transform">
              <ShieldCheck class="w-6 h-6" />
            </div>
            <div>
              <h4 class="text-white light-text-slate-900 font-bold mb-1 text-lg">{{ t('roadmap.focus.safe_title') }}</h4>
              <p class="text-slate-400 light-text-slate-600 text-sm leading-relaxed">
                 {{ t('roadmap.focus.safe_desc') }}
              </p>
            </div>
          </div>
        </div>
      </div>

      <!-- Commercial Strategy -->
      <div class="glass-card p-8 rounded-3xl border-slate-700/50">
        <h3 class="text-xl font-bold text-white light-text-slate-900 mb-6 flex items-center gap-2">
            <LayoutTemplate class="w-5 h-5 text-slate-400" />
            {{ t('roadmap.strategy.title') }}
        </h3>
        
        <div class="space-y-4">
          <!-- Community -->
          <div class="p-4 rounded-xl bg-green-500/10 border border-green-500/20 transition-colors hover:bg-green-500/20">
            <div class="flex justify-between items-center mb-2">
              <span class="font-bold text-green-400">{{ t('roadmap.strategy.comm_title') }}</span>
              <span class="text-[10px] font-bold bg-green-500/20 text-green-300 px-2 py-0.5 rounded uppercase">{{ t('roadmap.strategy.comm_badge') }}</span>
            </div>
            <p class="text-sm text-slate-400 light-text-slate-600">{{ t('roadmap.strategy.comm_desc') }}</p>
          </div>

          <!-- Pro -->
          <div class="p-4 pt-8 rounded-xl bg-purple-500/10 border border-purple-500/20 relative overflow-hidden transition-colors hover:bg-purple-500/20">
             <div class="absolute top-0 right-0 bg-purple-500/30 px-3 py-1 rounded-bl-xl text-[10px] font-bold text-purple-200 uppercase">Coming Soon</div>
            <div class="flex justify-between items-center mb-2">
              <span class="font-bold text-purple-400">{{ t('roadmap.strategy.pro_title') }}</span>
              <span class="text-[10px] font-bold bg-purple-500/20 text-purple-300 px-2 py-0.5 rounded uppercase">{{ t('roadmap.strategy.pro_badge') }}</span>
            </div>
            <p class="text-sm text-slate-400 light-text-slate-600">{{ t('roadmap.strategy.pro_desc') }}</p>
          </div>
        </div>
        
        <div class="mt-8 pt-6 border-t border-white/5 text-center">
            <p class="text-xs text-slate-500 font-mono">
                {{ t('roadmap.verified') }}
            </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
:global(body.light-mode) .glass-card {
  @apply bg-white/60 border-black/5 shadow-xl;
}
:global(body.light-mode) .light-text-slate-900 {
  @apply text-slate-900;
}
:global(body.light-mode) .light-text-slate-600 {
  @apply text-slate-600;
}
</style>
