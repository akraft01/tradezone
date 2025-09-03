<script setup>
const motion = {
  initial: { opacity: 0, y: 40 },
  enter: { opacity: 1, y: 0, transition: { delay: 0.2, duration: 0.6 } }
}
onMounted(() => {
  if (window.adsbygoogle && process.client) {
    try {
      (adsbygoogle = window.adsbygoogle || []).push({});
    } catch (e) {
      console.error("AdSense error", e)
    }
  }
})
</script>

<template>
  <div class="min-h-screen bg-gray-900 text-gray-100 font-sans">

<!-- NAVBAR -->
<nav class="flex justify-between items-center px-6 py-4 bg-gray-950 shadow-md sticky top-0 z-50 backdrop-blur">
  <NuxtLink to="/" class="text-xl font-bold tracking-tight text-white hover:text-indigo-400 transition">
    TradingLab<span class="text-indigo-400">.</span>
  </NuxtLink>
  <div class="flex gap-6 text-sm text-gray-300">
    <a href="#newsletter" class="hover:text-indigo-400 transition">Newsletter</a>
    <NuxtLink to="/articles" class="hover:text-indigo-400 transition">Articles</NuxtLink>
    <NuxtLink to="/about" class="hover:text-indigo-400 transition">About</NuxtLink>
    <NuxtLink to="/privacy-policy" class="hover:text-indigo-400 transition">Privacy Policy</NuxtLink>
  </div>
</nav>


    <!-- HERO -->
    <section class="relative py-32 bg-gradient-to-br from-gray-800 via-gray-900 to-black text-center overflow-hidden">
      <div class="absolute inset-0 opacity-10 bg-[url('/noise.png')] bg-cover pointer-events-none"></div>
      <Motion :initial="motion.initial" :enter="motion.enter">
        <div class="relative z-10 max-w-3xl mx-auto px-6">
          <h1 class="text-5xl md:text-6xl font-extrabold text-white leading-tight">
            Unlock Smart <span class="text-indigo-400">Trading Insights</span>
          </h1>
          <p class="mt-6 text-lg text-gray-300">
            Actionable articles, weekly analysis, and the mindset to trade better.
          </p>
          <div class="mt-8 flex justify-center gap-4 flex-wrap">
            <NuxtLink
  to="/articles"
  class="px-6 py-3 text-lg rounded-lg font-semibold bg-indigo-600 text-white hover:bg-indigo-500 transition duration-200 shadow-md hover:shadow-lg ring-1 ring-indigo-400/50 cursor-pointer"
>
  📘 Read Articles
</NuxtLink>
<a
  href="#newsletter"
  class="px-6 py-3 text-lg rounded-lg font-semibold border border-indigo-400 text-indigo-300 hover:bg-indigo-500 hover:text-white transition duration-200 shadow-md hover:shadow-lg cursor-pointer"
>
  📩 Join Newsletter
</a>
          </div>
        </div>
      </Motion>
    </section>


<!-- INCOMING SIMULATOR BANNER -->
<section class="bg-indigo-700 text-white py-6">
  <Motion :initial="motion.initial" :enter="motion.enter">
    <div class="max-w-3xl mx-auto px-6 text-center flex flex-col md:flex-row items-center justify-center gap-4">
      <p class="text-lg md:text-xl font-medium">
        🚧 We’re building a <span class="font-bold">Trading Simulator</span>—launching soon!
      </p>
      <NuxtLink
        to="#newsletter"
        class="inline-block px-5 py-2 bg-white text-indigo-700 rounded-md font-semibold hover:bg-gray-100 transition"
      >
        Subscribe to know when it arrives
      </NuxtLink>
    </div>
  </Motion>
</section>



<!-- HIGHLIGHTS -->
<section class="py-20 bg-gray-900 border-t border-gray-800">
  <div class="max-w-6xl mx-auto px-6 grid md:grid-cols-3 gap-10 text-center">
    <Motion :initial="motion.initial" :enter="{ ...motion.enter, transition: { delay: 0.1 } }">
      <div class="p-6 bg-gray-800 rounded-lg hover:shadow-lg hover:shadow-indigo-500/20 transition duration-300 transform hover:scale-[1.02]">
        <h3 class="text-2xl font-bold mb-2 text-indigo-400">🚀 Instant Alpha</h3>
        <p class="text-gray-400 text-sm">No fluff. Just high-impact trading insights that you can apply today.</p>
      </div>
    </Motion>

    <Motion :initial="motion.initial" :enter="{ ...motion.enter, transition: { delay: 0.3 } }">
      <div class="p-6 bg-gray-800 rounded-lg hover:shadow-lg hover:shadow-purple-500/20 transition duration-300 transform hover:scale-[1.02]">
        <h3 class="text-2xl font-bold mb-2 text-purple-400">📊 Zero Guesswork</h3>
        <p class="text-gray-400 text-sm">Data-driven strategies, simplified for real results — no jargon, just clarity.</p>
      </div>
    </Motion>

    <Motion :initial="motion.initial" :enter="{ ...motion.enter, transition: { delay: 0.5 } }">
      <div class="p-6 bg-gray-800 rounded-lg hover:shadow-lg hover:shadow-emerald-500/20 transition duration-300 transform hover:scale-[1.02]">
        <h3 class="text-2xl font-bold mb-2 text-emerald-400">🧠 Learn in 3 Minutes</h3>
        <p class="text-gray-400 text-sm">Bite-sized reads that sharpen your edge — perfect for busy minds.</p>
      </div>
    </Motion>
  </div>
</section>






    <!-- NEWSLETTER -->
    <section id="newsletter" class="py-20 bg-indigo-600 text-white text-center">
      <Motion :initial="motion.initial" :enter="motion.enter">
        <div class="max-w-2xl mx-auto px-4">
          <h2 class="text-3xl font-extrabold">📬 Join 1,000+ Readers</h2>
          <p class="mt-4 text-lg">
            Get one value-packed email each week — no fluff, just strategy.
          </p>
          <form class="mt-8 flex flex-col sm:flex-row justify-center gap-4">
            <input
  type="email"
  placeholder="Enter your email..."
  class="w-full sm:w-80 px-5 py-3 rounded-lg bg-gray-800 text-white placeholder-gray-400 border border-gray-600 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 transition duration-200"
/>
            <button
  type="submit"
  class="px-6 py-3 rounded-md text-lg font-semibold bg-white text-indigo-600 hover:bg-indigo-100 transition shadow-md hover:shadow-lg cursor-pointer"
>
  Subscribe
</button>
          </form>
        </div>
      </Motion>
    </section>


    
    <!-- FOOTER -->
    <footer class="py-10 bg-gray-900 text-center text-gray-500 text-sm border-t border-gray-800">
      © 2025 TradingLab. All rights reserved.
    </footer>
  </div>
</template>
