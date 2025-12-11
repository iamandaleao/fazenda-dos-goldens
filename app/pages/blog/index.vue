<template>
  <section class="pt-24 pb-16 max-w-6xl mx-auto px-4 md:px-6 lg:px-8">
    <div class="text-center mb-12">
      <h1 class="text-5xl font-bold text-amber-700 mb-3">
        🐕 Blog dos Goldens da Chácara
      </h1>
      <p class="text-gray-600 text-lg">
        Dicas, histórias e cuidados com nossos amigos de quatro patas
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-8 md:gap-10 lg:gap-12">
      <article
        v-for="post in posts"
        :key="post.slug"
        class="bg-white rounded-2xl shadow-md hover:shadow-xl transition-all duration-300 overflow-hidden border border-amber-100"
      >
        <img 
          :src="post.image" 
          :alt="post.title"
          class="w-full h-64 md:h-72 lg:h-80 object-cover object-center bg-gray-100"
        />
        
        <div class="p-6">
          <h2 class="text-2xl font-bold text-gray-900 mb-3 hover:text-amber-600 transition">
            {{ post.title }}
          </h2>
          
          <p class="text-gray-600 mb-4 leading-relaxed">
            {{ post.excerpt }}
          </p>

          <NuxtLink
            :to="`/blog/${post.slug}`"
            class="inline-block px-6 py-2.5 bg-amber-600 text-white font-semibold rounded-lg hover:bg-amber-700 transition"
          >
            Ler artigo completo →
          </NuxtLink>
        </div>
      </article>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

// Dados dos posts com imagens de placeholder
const posts = ref([
  {
    title: "Como escolher um Golden saudável",
    slug: "como-escolher-um-golden-saudavel",
    image: "https://placedog.net/800/600?id=1",
    excerpt: "Um guia completo para entender linhagem, saúde e comportamento ao escolher seu futuro companheiro...",
  },
  {
    title: "Primeiros cuidados com um filhote",
    slug: "primeiros-cuidados-filhote",
    image: "https://placedog.net/800/600?id=2",
    excerpt: "Dicas práticas e essenciais para garantir que seu filhote cresça feliz, saudável e bem adaptado à nova casa...",
  },
  {
    title: "Alimentação ideal para Golden Retriever",
    slug: "alimentacao-golden-retriever",
    image: "https://placedog.net/800/600?id=3",
    excerpt: "Descubra qual a melhor alimentação para cada fase da vida do seu Golden e mantenha ele sempre saudável...",
  },
  {
    title: "Exercícios e brincadeiras para Goldens",
    slug: "exercicios-brincadeiras-goldens",
    image: "https://placedog.net/800/600?id=4",
    excerpt: "Atividades divertidas e exercícios importantes para manter seu Golden ativo, feliz e com muita energia...",
  }
])
</script>