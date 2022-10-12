<script setup>
import { onBeforeUpdate, ref } from 'vue';

const isOpen = ref(false);
function menufunction() {
  isOpen.value = !isOpen.value;
}
function clickContent() {
  return (isOpen.value = false);
}

const showBar = ref(false);

window.onscroll = function () {
  scrollFunction();
};

function scrollFunction() {
  // console.log(document.documentElement.scrollTop);
  if (
    document.body.scrollTop > 100 ||
    document.documentElement.scrollTop > 100
  ) {
    showBar.value = true;
  } else {
    showBar.value = false;
  }
}
</script>

<template>
  <div class="flex-1 flex items-center text-red-700 font-mono z-50 w-full">
    <nav
      class="text-md font-semibold flex flex-wrap items-center justify-between w-full py-2 md:py-0 px-2 md:px-4 text-lg text-white drop-shadow-2xl"
      :class="{
        'shadow bgskill  transition duration-100': showBar,
      }"
    >
      <div>
        <a href="#">
          <div class="logo text-3xl shadow-solid-primary text4 pl-6 md:w-full">
            Portfolio
          </div>
        </a>
      </div>

      <div class="flex md:items-center md:w-auto" id="menu">
        <ul class="pt-4 text-base md:flex md:justify-between md:pt-0 hidden">
          <li>
            <a class="md:p-4 py-2 block hover:text-purple-400" href="#home"
              >Home</a
            >
          </li>
          <li>
            <a class="md:p-4 py-2 block hover:text-purple-400" href="#aboutme"
              >About Me</a
            >
          </li>
          <li>
            <a
              class="md:p-4 py-2 lg:block hidden hover:text-purple-400"
              href="#myskill"
              >Skill</a
            >
          </li>
          <li>
            <a
              class="md:p-4 py-2 block hover:text-purple-400"
              href="#experience"
              >Experience</a
            >
          </li>
          <li>
            <a
              class="md:p-4 py-2 lg:block hidden hover:text-purple-400"
              href="#certificate"
              >Certificate</a
            >
          </li>
        </ul>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          id="menu-button"
          class="h-6 w-6 cursor-pointer lg:hidden block mr-3"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          @click="menufunction()"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16"
          />
        </svg>
      </div>

      <aside
        class="transform text-black top-0 left-0 w-3/5 bg-white fixed h-screen overflow-auto ease-in-out transition-all duration-300 z-50 translate-x-0"
        :class="{
          '-translate-x-full': !isOpen,
        }"
      >
        <div class="pt-10 px-5 text-md">
          <div class="flex flex-col divide-y-2">
            <a href="#" class="py-3" @click="clickContent()"> Home </a>
            <a href="#aboutme" class="py-3" @click="clickContent()">
              About Me
            </a>
            <a href="#myskill" class="py-3" @click="clickContent()"> Skill </a>
            <a href="#experience" class="py-3" @click="clickContent()">
              Experience
            </a>
            <a href="#certificate" class="py-3" @click="clickContent()">
              Certificate
            </a>
          </div>
          <div class="flex justify-center pt-14" @click="clickContent()">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="40"
              height="40"
              fill="currentColor"
              class="bi bi-x-circle"
              viewBox="0 0 16 16"
            >
              <path
                d="M8 15A7 7 0 1 1 8 1a7 7 0 0 1 0 14zm0 1A8 8 0 1 0 8 0a8 8 0 0 0 0 16z"
              />
              <path
                d="M4.646 4.646a.5.5 0 0 1 .708 0L8 7.293l2.646-2.647a.5.5 0 0 1 .708.708L8.707 8l2.647 2.646a.5.5 0 0 1-.708.708L8 8.707l-2.646 2.647a.5.5 0 0 1-.708-.708L7.293 8 4.646 5.354a.5.5 0 0 1 0-.708z"
              />
            </svg>
          </div>
        </div>
      </aside>
      <aside
        class="top-0 right-0 w-full fixed h-screen bg-zinc-100/30 transition ease-in opacity-100 duration-700 z-20"
        :class="{ hidden: !isOpen }"
        @click="clickContent()"
      ></aside>
    </nav>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Rammetto+One&display=swap');

.logo {
  font-family: 'Rammetto One', cursive;
}

.text4 {
  text-shadow: 0px 4px 3px rgba(0, 0, 0, 0.4), 0px 8px 13px rgba(0, 0, 0, 0.1),
    0px 18px 23px rgba(0, 0, 0, 0.1);
}
</style>
