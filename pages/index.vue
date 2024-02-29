<script setup lang="ts">
useHead({
  title: 'Home',
  script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
})
</script>

<template>
  <main class="space-y-4">
    <h1 class="text-4xl">Welcome!</h1>
    <div class="space-y-4">
      <p>This template demonstrates the creation of a static site using:</p>
      <ul class="list-disc list-inside">
        <li>Nuxt 3</li>
        <li>Tailwind CSS</li>
        <li>Decap CMS (formerly Netlify)</li>
      </ul>
    </div>
    <div class="space-y-4">
      <h2 class="text-2xl">Posts</h2>
      <p>
        Posts are the core of this site:
        <NuxtLink to="/posts" class="underline text-blue-500">Click here</NuxtLink>
      </p>
    </div>
  </main>
</template>
