<template>
  <nav class="bg-white shadow-md">
    <div class="container mx-auto px-6 py-3 flex justify-between items-center">
      
      <!-- Logo + Nome -->
      <NuxtLink to="/" class="flex items-center space-x-3">
        <img
          src="~/assets/images/logo_linguesc.png"
          alt="Linguesc"
          class="h-10 w-auto"
        />
        <span class="text-2xl font-bold text-gray-800">
          Linguesc Hub
        </span>
      </NuxtLink>

      <!-- Navegação básica -->
      <div class="flex space-x-6 text-sm">
        <NuxtLink to="/" class="text-gray-700 hover:text-blue-500">
          Início
        </NuxtLink>
      </div>

    </div>
  </nav>
</template>

<script setup>
// Navbar simples, sem props por enquanto
</script>
