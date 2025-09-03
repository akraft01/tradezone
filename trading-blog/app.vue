<script setup>
useHead({
  script: [
    {
      async: true,
      src: "https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js",
      "data-ad-client": "pub-5841611579232239", // ← replace with your pub ID
      crossorigin: "anonymous"
    }
  ]
})
</script>

<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>




