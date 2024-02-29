<script setup lang="ts">
const route = useRoute()
const actualPath = route.path.replace(/\/$/, '')
const { data: post } = await useAsyncData('post', () => queryContent(actualPath).findOne())
</script>

<template>
  <main v-if="post" class="space-y-4">
    <NuxtLink to="/posts" class="underline text-blue-500">Back</NuxtLink>
    <h1 class="text-4xl">
      {{ post.title }}
    </h1>
    <p>{{ post.description }}</p>
    <ContentDoc />
  </main>
</template>
