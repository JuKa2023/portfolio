<template>
  <div class="flex px-6 flex-col md:flex-row md:items-start gap-x-16 space-x-0 md:space-x-8">
    <img :src="image" alt="Project Image" class="w-full md:w-1/3 shadow-md" />

    <div class="mb-4 md:w-2/3 flex flex-col justify-between h-full text-left">
      <h2 class="text-gray-700 text-2xl font-semibold underline underline-offset-16 text-left">
        {{ title }}
      </h2>

      <div class="flex space-x-4 my-8">
        <span
          v-for="tag in tags"
          :key="tag"
          class="bg-white text-gray-500 px-2 py-1 border rounded-3xl text-m"
        >
          {{ tag }}
        </span>
      </div>

      <p class="text-gray-700 flex-1 text-lg text-left">{{ description }}</p>

      <div class="flex gap-4 space-x-6 mt-8">
        <a :href="link" class="icon-button">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M12 21a9.004 9.004 0 0 0 8.716-6.747M12 21a9.004 9.004 0 0 1-8.716-6.747M12 21c2.485 0 4.5-4.03 4.5-9S14.485 3 12 3m0 18c-2.485 0-4.5-4.03-4.5-9S9.515 3 12 3m0 0a8.997 8.997 0 0 1 7.843 4.582M12 3a8.997 8.997 0 0 0-7.843 4.582m15.686 0A11.953 11.953 0 0 1 12 10.5c-2.998 0-5.74-1.1-7.843-2.918m15.686 0A8.959 8.959 0 0 1 21 12c0 .778-.099 1.533-.284 2.253m0 0A17.919 17.919 0 0 1 12 16.5c-3.162 0-6.133-.815-8.716-2.247m0 0A9.015 9.015 0 0 1 3 12c0-1.605.42-3.113 1.157-4.418" />
          </svg>

        </a>
        <a :href="github" class="icon-button">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
            <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
          </svg>
        </a>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps(['title', 'description', 'tags', 'image', 'link', 'github']);
</script>

<style>
.icon-button {
  padding: 0.75rem;
  background-color: white;
  border-radius: 9999px;
  border: 1px solid;
  border-color: #fb9973;
  transition-property: color, background-color, border-color;
  transition-duration: 200ms;
  box-shadow: 0 1px 2px 0 rgb(0 0 0 / 0.05);
  display: flex;
  align-items: center;
}

.icon-button:hover {
  background-color: rgb(250, 245, 243);
  border-color: #f7b397;
}
</style>