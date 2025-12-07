<template>
    <!-- Navigation -->
    <nav class="fixed w-full bg-white/95 backdrop-blur-sm shadow-sm z-40">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between items-center h-16">
          <div class="flex items-center">
            <span class="text-xl sm:text-2xl font-bold text-amber-600">Golden Farm</span>
          </div>
          
          <!-- Desktop Menu -->
          <div class="hidden md:flex space-x-6 lg:space-x-8">
            <a href="#inicio" class="text-gray-700 hover:text-amber-600 transition text-sm lg:text-base">Início</a>
            <a href="#sobre" class="text-gray-700 hover:text-amber-600 transition text-sm lg:text-base">Nossa História</a>
            <a href="#raca" class="text-gray-700 hover:text-amber-600 transition text-sm lg:text-base">A Raça</a>
            <a href="#valores" class="text-gray-700 hover:text-amber-600 transition text-sm lg:text-base">Valores</a>
            <a href="#contato" class="text-gray-700 hover:text-amber-600 transition text-sm lg:text-base">Contato</a>
          </div>

          <!-- Mobile menu button -->
          <button 
            @click="mobileMenuOpen = !mobileMenuOpen" 
            class="md:hidden p-2"
            aria-label="Menu"
          >
            <X v-if="mobileMenuOpen" :size="24" />
            <Menu v-else :size="24" />
          </button>
        </div>
      </div>

      <!-- Mobile Menu -->
      <div v-if="mobileMenuOpen" class="md:hidden bg-white border-t">
        <div class="px-4 pt-2 pb-3 space-y-1">
          <a 
            href="#inicio" 
            @click="mobileMenuOpen = false"
            class="block px-3 py-2 text-gray-700 hover:bg-amber-50 rounded"
          >
            Início
          </a>
          <a 
            href="#sobre" 
            @click="mobileMenuOpen = false"
            class="block px-3 py-2 text-gray-700 hover:bg-amber-50 rounded"
          >
            Nossa História
          </a>
          <a 
            href="#raca" 
            @click="mobileMenuOpen = false"
            class="block px-3 py-2 text-gray-700 hover:bg-amber-50 rounded"
          >
            A Raça
          </a>
          <a 
            href="#valores" 
            @click="mobileMenuOpen = false"
            class="block px-3 py-2 text-gray-700 hover:bg-amber-50 rounded"
          >
            Valores
          </a>
          <a 
            href="#contato" 
            @click="mobileMenuOpen = false"
            class="block px-3 py-2 text-gray-700 hover:bg-amber-50 rounded"
          >
            Contato
          </a>
        </div>
      </div>
    </nav>
</template>

<script setup>
const mobileMenuOpen = ref(false)
</script>
