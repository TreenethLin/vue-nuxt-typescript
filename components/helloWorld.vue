<template>
  <div class="min-h-screen bg-gradient-to-br from-indigo-500 to-purple-600 flex items-center justify-center">
    <div class="bg-white rounded-lg shadow-xl p-8 max-w-md w-full">
      <h1 class="text-3xl font-bold text-gray-800 mb-6 text-center">
        {{ greeting }}
      </h1>
      <div class="bg-gray-100 rounded-lg p-6 mb-6">
        <p class="text-xl text-gray-700 font-semibold text-center">
          Count: <span class="text-indigo-600">{{ count }}</span>
        </p>
      </div>
      <button 
        @click="incrementCount"
        class="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3 px-4 rounded-lg transition duration-300 ease-in-out transform hover:scale-105 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-opacity-50"
      >
        Increment
      </button>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const greeting = ref('Hello, Vue with Nuxt and TypeScript!')
const count = ref(0)

const incrementCount = () => {
  count.value++
}
</script>