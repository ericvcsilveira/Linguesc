<template>
  <div class="min-h-screen flex bg-gray-200">
    <Sidebar :open="sidebarOpen" @toggle="toggleSidebar" />

    <div class="flex-1 flex flex-col transition-all duration-300">

      <main class="flex-1 p-6">
        <slot />
      </main>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Sidebar from '~/components/Sidebar.vue'

const sidebarOpen = ref(true)

function toggleSidebar() {
  sidebarOpen.value = !sidebarOpen.value
}
</script>
