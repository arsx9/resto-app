
<script setup>
import { ref } from 'vue'

const count = ref(0)
</script>

<template>
  <div class="min-h-screen bg-gray-100 flex items-center justify-center p-6">
    <div class="bg-white rounded-2xl shadow-xl p-8 max-w-md w-full text-center">

      <h1 class="text-3xl font-bold text-blue-600 mb-4">
        Vue + Tailwind CSS
      </h1>

      <p class="text-gray-600 mb-6">
        If you can see this styled card, Tailwind is working!
      </p>

      <button
        @click="count++"
        class="bg-blue-600 hover:bg-blue-700 text-white font-semibold px-6 py-3 rounded-lg transition"
      >
        Click Me: {{ count }}
      </button>

      <div class="mt-6 p-3 bg-green-100 text-green-700 rounded-lg font-medium">
        Tailwind CSS is working!
      </div>

    </div>
  </div>
</template>