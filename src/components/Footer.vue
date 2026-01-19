<script setup lang="ts">
import { Github, Twitter } from 'lucide-vue-next'

const curYear = new Date().getFullYear()
</script>

<template>
  <footer class="py-12 border-t border-white/5 bg-slate-900/50 relative z-10 w-full">
    <div class="max-w-7xl mx-auto px-6 flex flex-col md:flex-row justify-between items-center gap-6">
      
      <!-- Brand -->
      <div class="flex items-center gap-3">
        <div class="w-8 h-8 bg-gradient-to-br from-indigo-500 to-purple-600 rounded-lg flex items-center justify-center p-1.5">
          <img src="/favicon.png" alt="Logo" class="w-full h-full object-contain">
        </div>
        <div class="text-sm text-slate-400">
          <span class="font-bold text-white light-text-slate-900">The Andb</span>
          <span class="mx-2">•</span>
          © {{ curYear }} Ph4n4n
        </div>
      </div>

      <!-- Links -->
      <div class="flex items-center gap-6 text-sm text-slate-500">
        <a href="https://github.com/The-Andb/andb" class="hover:text-white transition-colors flex items-center gap-2">
          <Github class="w-4 h-4" /> GitHub
        </a>
        <a href="https://twitter.com/ph4n4n" class="hover:text-white transition-colors flex items-center gap-2">
          <Twitter class="w-4 h-4" /> Twitter
        </a>
      </div>

    </div>
  </footer>
</template>

<style scoped>
:global(body.light-mode) .light-text-slate-900 {
  @apply text-slate-900;
}
</style>
