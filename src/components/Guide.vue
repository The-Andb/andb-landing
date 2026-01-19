<script setup lang="ts">
import { useI18n } from 'vue-i18n'
import { HelpCircle, ArrowRight, ShieldAlert, CheckCircle, Copy } from 'lucide-vue-next'
import { ref } from 'vue'

const { t } = useI18n()
const copied = ref(false)
const fixCommand = 'xattr -cr /Applications/The\\ Andb.app'

const copyCommand = () => {
    navigator.clipboard.writeText(fixCommand)
    copied.value = true
    setTimeout(() => copied.value = false, 2000)
}
</script>

<template>
  <section id="guide" class="max-w-4xl mx-auto mb-20 px-4">
    <!-- Links -->
    <div class="mb-10 text-center">
      <a href="https://github.com/The-Andb/andb/blob/main/README.md" target="_blank"
        class="text-sm text-slate-400 hover:text-indigo-400 transition-colors flex items-center justify-center gap-2 group">
        <HelpCircle class="w-4 h-4 text-indigo-500/50 group-hover:text-indigo-500 transition-colors" />
        {{ t('guide.setup_link') }} <span class="underline underline-offset-4 decoration-indigo-500/30 group-hover:decoration-indigo-500">{{ t('guide.view_guide') }}</span>
      </a>
    </div>

    <!-- Troubleshooting macOS Section -->
    <div class="rounded-3xl bg-slate-900/50 border border-slate-700/50 backdrop-blur-xl text-left relative overflow-hidden group p-6 md:p-8">
      <!-- Glow effect -->
      <div class="absolute -top-24 -right-24 w-48 h-48 bg-amber-500/10 blur-[60px] rounded-full group-hover:bg-amber-500/20 transition-colors duration-700"></div>

      <div class="flex flex-col md:flex-row items-start gap-6 relative z-10">
        <div class="p-3 bg-amber-500/10 rounded-2xl shrink-0 border border-amber-500/20 shadow-lg shadow-amber-500/5">
          <ShieldAlert class="w-6 h-6 text-amber-500" />
        </div>
        <div class="flex-1 w-full">
          <h4 class="text-slate-100 light-text-slate-900 font-bold text-lg mb-1 flex items-center gap-2">
            {{ t('guide.mac_fix_title') }}
          </h4>
          <p class="text-sm text-slate-400 light-text-slate-600 leading-relaxed mb-4 font-light">
             {{ t('guide.mac_fix_desc') }}
          </p>
          <p class="text-sm text-slate-400 light-text-slate-600 leading-relaxed mb-4 font-light">
            {{ t('guide.mac_fix_step') }} <span class="text-indigo-400 font-medium">Terminal.app</span>:
          </p>

          <div class="relative group/code">
            <div class="bg-black/60 rounded-xl p-4 font-mono text-sm inline-flex w-full items-center justify-between border border-white/5 group-hover/code:border-indigo-500/30 transition-all shadow-inner">
              <code class="text-indigo-300 break-all pr-4">{{ fixCommand }}</code>
              <button @click="copyCommand" class="shrink-0 p-2 hover:bg-white/10 rounded-lg transition-all active:scale-95 text-slate-400 hover:text-white relative">
                <Copy class="w-4 h-4" />
                <span v-if="copied" class="absolute -top-10 left-1/2 -translate-x-1/2 bg-indigo-600 text-white text-[10px] px-2 py-1 rounded transition-all">Copied!</span>
              </button>
            </div>
          </div>

          <div class="mt-5 flex flex-col sm:flex-row items-start sm:items-center justify-between gap-4 pt-4 border-t border-white/5">
            <p class="text-[11px] text-slate-500 flex items-center gap-2">
              <CheckCircle class="w-3 h-3 text-green-500/50" />
              {{ t('guide.mac_fix_note') }}
            </p>
            <a href="https://github.com/The-Andb/andb/blob/main/README.md" target="_blank"
              class="inline-flex items-center gap-2 px-4 py-2 bg-indigo-500/10 hover:bg-indigo-500/20 text-indigo-300 rounded-xl text-sm font-semibold transition-all border border-indigo-500/20 hover:border-indigo-500/40 group/guide">
              {{ t('guide.full_guide_btn') }}
              <ArrowRight class="w-4 h-4 transition-transform group-hover/guide:translate-x-1" />
            </a>
          </div>
        </div>
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
