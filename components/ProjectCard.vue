<template>
  <div class="flex flex-col md:flex-row items-center md:items-start space-x-0 md:space-x-8">
    <!-- Image on the left -->
    <img :src="image" alt="Project Image" class="w-full md:w-1/3 shadow-md mb-8" />

    <!-- Text content on the right -->
    <div class="mb-4 md:w-2/3 flex flex-col justify-between h-full">
      <!-- Title -->
      <h2 class="text-gray-700 text-2xl font-semibold underline underline-offset-16">
        {{ title }}
      </h2>

      <!-- Tags -->
      <div class="flex space-x-4 my-8">
        <span
          v-for="tag in tags"
          :key="tag"
          class="bg-white px-2 py-1 border rounded-3xl text-m"
        >
          {{ tag }}
        </span>
      </div>

      <!-- Description -->
      <p class="text-gray-700 flex-1 text-lg">{{ description }}</p>

      <!-- Link (aligned at the bottom) -->
      <a :href="link" class="text-gray-700 hover:text-purple-500 underline underline-offset-8 mt-8 text-lg inline-block">Webseite Besuchen</a>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps(['title', 'description', 'tags', 'image', 'link']);
</script>