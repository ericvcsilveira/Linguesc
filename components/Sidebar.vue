<template>
  <aside
    :class="[
      'bg-white shadow-md h-screen fixed top-0 left-0 z-40 transition-all duration-300',
      open ? 'w-72' : 'w-16'
    ]"
  >
    <!-- Logo -->
    <div
    :class="[
        'flex items-center p-4 border-b',
        open ? 'justify-between' : 'justify-center'
    ]"
    >
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
  <div :class="open ? 'w-72' : 'w-16'"></div>
</template>

<script setup>
defineProps({
  open: Boolean
})
</script>
