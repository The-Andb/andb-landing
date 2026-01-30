<template>
  <section class="py-20">
    <div class="max-w-4xl mx-auto px-4">
      <div class="glass-panel p-10 md:p-14 rounded-3xl text-center bg-gradient-to-b from-blue-500/5 to-transparent border-blue-500/10">
        <h2 class="text-3xl font-bold mb-6">Your Data <span class="text-blue-400">Never</span> Leaves Your Mac</h2>
        <p class="text-gray-400 text-lg mb-8 max-w-2xl mx-auto leading-relaxed">
          The Andb connects directly from your machine to your database via native drivers.
          There is no intermediary cloud server, no tracking pixels on your schema, and no SaaS subscription required for core features.
        </p>

        <div class="flex justify-center gap-4 text-sm font-mono text-gray-500">
          <div class="px-3 py-1 bg-white/5 rounded border border-white/5">Localhost:5432</div>
          <span class="text-gray-600">--[ TLS ]--></span>
          <div class="px-3 py-1 bg-white/5 rounded border border-white/5">Prod DB</div>
        </div>
      </div>
    </div>
  </section>
</template>
