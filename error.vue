<script setup>
const props = defineProps({
  error: Object
})
</script>

<template>
    <div>
      <div class="container">
        <h1>{{ error.statusCode }}</h1>
        <h2 class="text-2xl">{{ error.statusMessage }} 😕</h2>
        <NuxtLink class="nuxtlink" to="/restaurants"> Go Back </NuxtLink>
      </div>
    </div>
  </template>
  
  
  <style scoped>
  
    .container {
      height: 60vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-evenly;
    }

    h1 {
      font-size: 4em;
    }
    .nuxtlink {
      color: white;
      background-color: rgb(20, 184, 166);
      padding: 15px;
      border-radius: 12px;
      font-weight: bold;
    }
  
  </style>