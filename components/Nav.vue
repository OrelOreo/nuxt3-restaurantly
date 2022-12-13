<template>
    <nav class="flex items-center justify-between flex-wrap bg-teal-500 p-6">
     <div class="flex items-center flex-shrink-0 text-white mr-6">
        <a href="/" class="font-semibold text-xl tracking-tight">Restaurantly</a>
    </div>

  <div class="w-full block lg:flex lg:items-center lg:w-auto">
    <div class="text-sm lg:flex-grow">
      <NuxtLink aria-current="page" to="/" class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4">
        Home
      </NuxtLink>
      <NuxtLink to="/restaurants" class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4">
        Restaurants
      </NuxtLink>
    </div>
  </div>
</nav>
</template>

<style scoped>
  nav {
    margin-bottom: 2rem;
  }
</style>