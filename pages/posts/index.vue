<script setup lang="ts">
const { data: posts } = await useAsyncData('posts', () => {
  return queryContent('/posts').find()
})
</script>

<template>
  <main>
    <h1 class="text-4xl mb-4">Posts</h1>
    <ul class="list-disc list-inside">
      <li v-for="post of posts" :key="post.slug">
        <NuxtLink :to="post._path" class="underline text-blue-500">{{ post.title }}</NuxtLink>
      </li>
    </ul>
  </main>
</template>
