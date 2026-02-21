<script setup>
import { ref } from 'vue'

const bio = ref({
name: 'Richard Montalvo',
avatar: 'https://api.dicebear.com/9.x/fun-emoji/svg?seed=Brian',
about: 'Theres not much to so really but im just a normal student who likes playing games, listening to music, and playing my instruments on my freetime.',
skills: ['Playing the Guitar, Bass, and Drums'],
email: 'rmonta23@stu.southtexascollege.edu',
location: 'Mcallen, Tx',
})

</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8 sm:py-12">
     <RouterLink
       to="/"
       class="my-8 self-start text-sm text-gray-400 underline-offset-4 transition-colors duration-200 hover:text-green-400 hover:underline"
      > Back to Links 
    </RouterLink>


<!-- Profile Card -->
 <div class="w-full max-w-lg border border-gray-700 bg-gray-800 p-6 shadow-xl shadow-gray-900/50 sm:p-8"
 >
<!-- Header -->
<div class="mb-6 flex flex-col items-center text-center sm:text-left">
  <div 
    class="mb-4 h-20 w=20 shrink-0 overflow-hidden rounded-full border-4 border-green-400 sm:mb-0 sm:mr-6"
    >
  
    <img 
    :src="bio.avatar" 
    :alt="bio.name"
    class="h-full w-full object-cover"
  >
  </div>
</div>
  <div>
    <h1 class="font-display text-2xl font-bold text-white">{{ bio.name }}</h1>
    <p class="text-sm text-grey-400">{{ bio.location }}</p>
  </div>

  <!-- About Section -->
  <div>
    <h2 class="mb-3 text-lg font-semibold text-white">About</h2>
    <p class="leading-relaxed text-gray-300">{{ bio.about }}</p>
  </div>
</div>
  </main>
</template>
