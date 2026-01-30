<template>
  <section class="py-32 relative" id="features">
    <div class="container mx-auto px-4">
      <div class="text-center max-w-2xl mx-auto mb-20">
        <h2 class="text-3xl font-bold tracking-tight mb-4">
          <span class="text-blue-400">The Power</span> of Precision
        </h2>
        <p class="text-gray-400">
          Built for teams that demand 100% database integrity.
          No more accidental drops. No more syntax errors in Production.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <!-- Feature 1: Semantic Diff -->
        <div class="glass-panel p-8 rounded-2xl hover:border-blue-500/30 transition-all group">
          <div class="w-12 h-12 bg-blue-500/10 rounded-lg flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
             <svg class="w-6 h-6 text-blue-400" viewBox="0 0 24 24" fill="none" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"></path></svg>
          </div>
          <h3 class="text-xl font-semibold mb-3">Semantic Comparison</h3>
          <p class="text-gray-400 text-sm leading-relaxed">
            We don't just compare text lines. Our engine parses the AST to understand that
            <code class="text-blue-300">INT</code> and <code class="text-blue-300">INTEGER</code> are the same, eliminating false positives.
          </p>
        </div>

        <!-- Feature 2: Safety Gates -->
        <div class="glass-panel p-8 rounded-2xl hover:border-green-500/30 transition-all group">
           <div class="w-12 h-12 bg-green-500/10 rounded-lg flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
             <svg class="w-6 h-6 text-green-400" viewBox="0 0 24 24" fill="none" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path></svg>
          </div>
          <h3 class="text-xl font-semibold mb-3">Safety Guardrails</h3>
          <p class="text-gray-400 text-sm leading-relaxed">
            Automatic snapshotting before migration. Dry-run support.
            Warning dialogs for destructive operations (<code class="text-red-400">DROP</code>, <code class="text-red-400">TRUNCATE</code>).
          </p>
        </div>

        <!-- Feature 3: Multi-Environment -->
        <div class="glass-panel p-8 rounded-2xl hover:border-purple-500/30 transition-all group">
           <div class="w-12 h-12 bg-purple-500/10 rounded-lg flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
             <svg class="w-6 h-6 text-purple-400" viewBox="0 0 24 24" fill="none" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10"></path></svg>
          </div>
          <h3 class="text-xl font-semibold mb-3">Environment Sync</h3>
          <p class="text-gray-400 text-sm leading-relaxed">
            Define Pairs (Dev -> Stage, Stage -> Prod).
            Sync schemas with one click. Maintain consistency across your entire pipeline.
          </p>
        </div>

      </div>
    </div>
  </section>
</template>
