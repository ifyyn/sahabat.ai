<script setup>
import Author from '@/components/Author.vue';
import { RouterLink } from 'vue-router';
import Button from '@/components/Button.vue';

</script>

<template>
  <main class="h-[400px] xl:mt-40 mt-20 justify-between text-center">
   <div class="xl:flex">
    <div class="">
      <img src="../assets/img/image1.jpeg" alt="" class="mx-auto">
    </div>
    <div class="xl:mt-20 mt-10">
      <h1 class="xl:text-6xl text-5xl font-bold bg-gradient-to-br rounded-md from-[#438eb5] to-white bg-clip-text text-transparent">Selamat Datang di Sahabat.Ai</h1>
      <p class="text-zinc-500 mt-2">"Temukan Ketenangan, Kembalikan Keseimbangan"</p>
      <RouterLink to="/chatbot">
        <Button class="mt-4 bg-[#151515]">Get Started</Button>
      </RouterLink>
    </div>
   </div>
  </main>
  <div class=" mt-60 xl:mt-10 text-center xl:text-start">
    <h1 class="text-2xl mb-5 p-3 text-[#438eb5] font-bold">About</h1>
    <ul class="p-3">
      <li class="text-justify mb-4">
        "Chatbot kami dirancang untuk memberikan dukungan emosional dan mental kapan saja Anda membutuhkannya. Dengan respons cepat dan anonim, Anda bisa berbagi apa saja tanpa rasa khawatir."
      </li>
      <li class="text-justify mb-4">
        "Kami menyediakan akses ke berbagai sumber daya kesehatan mental, termasuk konseling dan teknik relaksasi yang dapat membantu Anda mengatasi stres dan kecemasan."
      </li>
      <li class="text-justify">
        "Chatbot kami belajar dari interaksi Anda untuk memberikan saran yang lebih tepat dan relevan, membantu Anda menemukan ketenangan dan kesejahteraan yang Anda butuhkan."
      </li>
    </ul>
   </div>
  <div class="h-[300px] xl:mt-0 mt-28">
    <Author/>
  </div>
</template>
