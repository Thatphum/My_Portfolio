<script setup>
import { ref } from 'vue';
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
import Home from './components/Home.vue';
import AboutMe from './components/AboutMe.vue';
import Skill from './components/Skill.vue';
import WorkExperience from './components/WorkExperience.vue';
import Certificate from './components/Certificate.vue';
</script>

<template>
  <div class="bg-gray-200 flex">
    <div class="flex-grow bg-white">
      <div class="flex h-12 sticky top-0">
        <Navbar />
      </div>
      <!-- content -->
      <main class="w-full pb-4">
        <Home />

        <!-- <span
          class="inline-flex px-2 py-0 rounded mb-8 text-xs uppercase bg-indigo-200 text-indigo-600 font-semibold"
          >Scroll down</span
        > -->
        <!-- 
        <p class="mb-8 text-sm text-gray-600">
          Made with TailwindCSS & Alpine.js.
        </p> -->
        <AboutMe />
        <Skill />
        <WorkExperience />
        <Certificate />
      </main>
    </div>
  </div>
  <Footer />
  <!-- content -->

  <!-- <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" /> -->
</template>

<style>
.bg-images {
  background-image: url('./assets/imgs/bg-home.png');
}
.text-color-main {
  color: rgb(0, 138, 193);
}
.bgskill {
  background: rgb(0, 138, 193);
}
html {
  scroll-behavior: smooth;
}
</style>
