<template>
    <section id="contact" class="w-full bg-purple-100 py-20">
        <div class="container mx-auto px-6">
            <div class="max-w-3xl px-6 mx-auto text-center">
                <h2 class="text-3xl font-bold text-gray-800 mb-6">Möchtest du mir was mitteilen?</h2>
                <div class="mt-6 text-lg text-gray-700">
                    <p class="mb-4">Ich würde mich freuen von dir zu hören.</p>
                    <p class="mb-8">
                        Schicke mir eine Email unter 
                        <a href="mailto:juliette.kauflin@gmail.com" class="text-purple-600 hover:text-purple-800 font-medium transition-colors duration-200">
                            juliette.kauflin@gmail.com
                        </a>
                    </p>
                </div>
                
                <div class="mt-10 flex flex-wrap justify-center gap-6">
                    <a href="/resume.pdf" class=" icon-text-button px-6 py-3 text-gray-700 font-medium rounded-full border flex items-center">
                        Resume
                    </a>
                    <a href="https://github.com/JuKa2023" class=" icon-text-button px-6 py-3 text-gray-700 font-medium rounded-full border flex items-center">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                        </svg>
                        Github
                    </a>
                    <a href="https://www.linkedin.com/in/juliette-k-7783b8158/" class=" icon-text-button px-6 py-3 text-gray-700 font-medium rounded-full border flex items-center">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
                        </svg>
                        LinkedIn
                    </a>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
</script>

<style>
.icon-text-button {
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

.icon-text-button:hover {
  background-color: rgb(250, 245, 243);
  border-color: #f7b397;
}
</style>