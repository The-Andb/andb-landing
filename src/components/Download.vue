<template>
  <section class="py-20 relative text-center" id="download">
    <div class="absolute inset-0 z-[-1] overflow-hidden">
      <div class="absolute bottom-[20%] left-[50%] -translate-x-1/2 w-[600px] h-[300px] bg-blue-500/10 rounded-full blur-[100px]"></div>
    </div>

    <div class="max-w-2xl mx-auto px-4">
      <h2 class="text-3xl md:text-5xl font-bold mb-8">Ready to feel <span class="text-blue-400">safe</span> again?</h2>
      <p class="text-gray-400 text-lg mb-12">
        Join 10,000+ developers who trust The Andb to manage their database changes. It's free to try.
      </p>

      <div class="flex flex-col sm:flex-row gap-4 justify-center">
        <button class="px-8 py-4 bg-white hover:bg-gray-100 text-black rounded-xl font-bold transition-all hover:scale-105 active:scale-95 shadow-xl shadow-white/5">
          Download beta for macOS
          <span class="block text-xs font-normal text-gray-500 mt-1">Apple Silicon (M1/M2/M3)</span>
        </button>
        <button class="px-8 py-4 bg-gray-800 hover:bg-gray-700 text-white rounded-xl font-bold transition-all border border-gray-700">
           Download for Intel
          <span class="block text-xs font-normal text-gray-500 mt-1">Universal Binary</span>
        </button>
      </div>

      <div class="mt-8 text-sm text-gray-500">
        Also available via <code class="bg-white/5 px-2 py-1 rounded text-blue-300">brew install --cask the-andb</code>
      </div>
    </div>
  </section>
</template>
