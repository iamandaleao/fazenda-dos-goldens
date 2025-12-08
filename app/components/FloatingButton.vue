<template>
  <!-- WhatsApp Floating Button -->
  <button
    class="fixed bottom-6 right-6 z-50 bg-green-500 text-white p-4 rounded-full shadow-lg hover:bg-green-600 transition-all hover:scale-110"
    aria-label="Contato via WhatsApp"
    @click="handleWhatsAppClick"
  >
    <MessageCircle :size="28" />
  </button>
</template>

<script setup>
import { MessageCircle } from 'lucide-vue-next'

// Configuração do WhatsApp
// IMPORTANTE: Substitua pelo seu número real no formato: 5537999999999
const whatsappNumber = '5537999999999'
const whatsappMessage = 'Olá! Tenho interesse nos filhotes de Golden Retriever 🐕'

const handleWhatsAppClick = () => {
  const url = `https://wa.me/${whatsappNumber}?text=${encodeURIComponent(whatsappMessage)}`
  window.open(url, '_blank')
}
</script>
