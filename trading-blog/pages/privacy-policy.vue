<script setup>

// Reuse the same motion settings as on the index page.
const motion = {
  initial: { opacity: 0, y: 40 },
  enter: { opacity: 1, y: 0, transition: { delay: 0.2, duration: 0.6 } }
}
</script>

<template>
  <div class="min-h-screen bg-gray-900 text-gray-100 font-sans">
<!-- NAVBAR -->
<nav class="flex justify-between items-center px-6 py-4 bg-gray-950 shadow-md sticky top-0 z-50 backdrop-blur">
  <NuxtLink to="/" class="text-xl font-bold tracking-tight text-white hover:text-indigo-400 transition">
    TradingLab<span class="text-indigo-400">.</span>
  </NuxtLink>
  <div class="flex gap-6 text-sm text-gray-300">
    <NuxtLink to="/" class="hover:text-indigo-400 transition">Home</NuxtLink>
    <NuxtLink to="/articles" class="hover:text-indigo-400 transition">Articles</NuxtLink>
    <NuxtLink to="/about" class="hover:text-indigo-400 transition">About</NuxtLink>
    <NuxtLink to="/privacy-policy" class="hover:text-indigo-400 transition">Privacy Policy</NuxtLink>
  </div>
</nav>


<!-- INCOMING SIMULATOR BANNER -->
<section class="bg-indigo-700 text-white py-6">
  <Motion :initial="motion.initial" :enter="motion.enter">
    <div class="max-w-3xl mx-auto px-6 text-center flex flex-col md:flex-row items-center justify-center gap-4">
      <p class="text-lg md:text-xl font-medium">
        🚧 We’re building a <span class="font-bold">Trading Simulator</span>—launching soon!
      </p>
      <NuxtLink
        to="http://localhost:3000/#newsletter"
        class="inline-block px-5 py-2 bg-white text-indigo-700 rounded-md font-semibold hover:bg-gray-100 transition"
      >
        Subscribe to know when it arrives
      </NuxtLink>
    </div>
  </Motion>
</section>

    <!-- FOOTER -->
    <footer class="py-10 bg-gray-900 text-center text-gray-500 text-sm border-t border-gray-800">
      © 2025 TradingLab. All rights reserved.
    </footer>
  </div>
</template>
