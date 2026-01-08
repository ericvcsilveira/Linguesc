<template>
  <aside
    :class="[
      'bg-white shadow-md h-screen fixed top-0 left-0 z-40 transition-all duration-300',
      open ? 'w-64' : 'w-16'
    ]"
  >
    <!-- Logo -->
    <div
    :class="[
        'flex items-center p-4 border-b',
        open ? 'justify-between' : 'justify-center'
    ]"
    >
    <span
        v-if="open"
        class="text-xl font-bold text-green-600"
    >
        Linguesc
    </span>

    <button
        @click="$emit('toggle')"
        class="text-gray-600 text-xl focus:outline-none"
    >
        ☰
    </button>
    </div>


    <!-- Menu -->
    <nav class="mt-6 space-y-2 px-2">
      <SidebarItem to="/hub" label="Início" icon="🏠" :open="open" />
      <SidebarItem to="/presenca" label="Presença" icon="📅" :open="open" />
      <SidebarItem to="/notas" label="Notas" icon="📊" :open="open" />
      <SidebarItem to="/perfil" label="Perfil" icon="👤" :open="open" />
    </nav>
  </aside>

  <!-- Espaçamento quando sidebar é fixa -->
  <div :class="open ? 'w-64' : 'w-16'"></div>
</template>

<script setup>
defineProps({
  open: Boolean
})
</script>
