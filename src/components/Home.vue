<script setup></script>

<template>
  <div class="header z-0" id="home">
    <!--Content before waves-->
    <div class="inner-header flex">
      <!-- start -->
      <div
        class="flex flex-col flex-col-reverse md:flex-row m-auto place-items-center place-content-center pt-20 "
      >
        <div class="py-2 text-center md:text-left w-2/3 md:w-1/3 md:pr-14">
          <h2 class="text-3xl md:text-6xl font-bold">Hi, I'm Thatphum</h2>
          <!-- <h2 class="text-3xl md:text-6xl font-bold">
            Thatphum Kongnithichalerm
          </h2> -->
          <h2 class="text-white text-4xl pt-2 font-bold">
            Full Stack Developer
          </h2>
          <p class="text-lg text-cyan-300 pt-2 font-bold">
            However difficult life may seem, there is always something you can
            do and succeed at. - Theory of Everything
          </p>
          <div class="pt-4">
            <a
              href="#aboutme"
              class="bg-white hover:bg-blue-700 text-blue-500 font-bold py-2 px-5 rounded-full"
            >
              About Me ->
            </a>
            <!-- <a
              href=""
              class="hover:bg-blue-700 text-white font-bold py-1.5 px-5 rounded-full outline outline-offset-2 outline-1 ml-4"
              >dsamdkla -></a
            > -->
            <!-- <a href="">read more.</a> -->
          </div>
        </div>
        <img
          src="../assets/imgs/Profile-01.png"
          alt="ModExchange"
          class="w-4/5 md:w-1/3 rounded-lg"
        />
      </div>
      <!-- end -->
    </div>

    <!--Waves Container-->
    <div>
      <svg
        class="waves"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        viewBox="0 24 150 28"
        preserveAspectRatio="none"
        shape-rendering="auto"
      >
        <defs>
          <path
            id="gentle-wave"
            d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z"
          />
        </defs>
        <g class="parallax">
          <use
            xlink:href="#gentle-wave"
            x="48"
            y="0"
            fill="rgba(255,255,255,0.7"
          />
          <use
            xlink:href="#gentle-wave"
            x="48"
            y="3"
            fill="rgba(255,255,255,0.5)"
          />
          <use
            xlink:href="#gentle-wave"
            x="48"
            y="5"
            fill="rgba(255,255,255,0.3)"
          />
          <use xlink:href="#gentle-wave" x="48" y="7" fill="#fff" />
        </g>
      </svg>
    </div>
    <!--Waves end-->
  </div>
  <!-- Header ends -->
</template>

<style scoped>
/* @import url('https://fonts.googleapis.com/css2?family=Kanit:wght@700&display=swap');
.name {
  font-family: 'Kanit', sans-serif;
}

.oval {
  border-radius: 180px 80px 200px 170px;
  background-image: url('../assets/imgs/Profile.jpg');
}

.bgprofile {
  background-image: url('../assets/imgs/2-01.png');
} */

@import url(//fonts.googleapis.com/css?family=Lato:300:400);
@import url('https://fonts.googleapis.com/css2?family=Fredoka+One&display=swap');

body {
  margin: 0;
}

h1 {
  font-family: 'Lato', sans-serif;
  font-weight: 300;
  letter-spacing: 2px;
  font-size: 48px;
}

.header {
  position: static;
  text-align: center;
  background: linear-gradient(
    60deg,
    rgba(84, 58, 183, 1) 0%,
    rgba(0, 172, 193, 1) 100%
  );
  color: white;
  margin-top: -3rem;
}
.logo {
  width: 50px;
  fill: white;
  padding-right: 15px;
  display: inline-block;
  vertical-align: middle;
}

.inner-header {
  height: 70%;
  width: 100%;
  margin: 0;
  padding: 0;
}

.flex {
  /*Flexbox for containers*/
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.waves {
  position: static;
  width: 100%;
  height: 15vh;
  margin-bottom: -7px; /*Fix for safari gap*/
  min-height: 100px;
  max-height: 150px;
}

.content {
  position: relative;
  height: 20vh;
  text-align: center;
  background-color: white;
}

/* Animation */

.parallax > use {
  animation: move-forever 25s cubic-bezier(0.55, 0.5, 0.45, 0.5) infinite;
}
.parallax > use:nth-child(1) {
  animation-delay: -2s;
  animation-duration: 7s;
}
.parallax > use:nth-child(2) {
  animation-delay: -3s;
  animation-duration: 10s;
}
.parallax > use:nth-child(3) {
  animation-delay: -4s;
  animation-duration: 13s;
}
.parallax > use:nth-child(4) {
  animation-delay: -5s;
  animation-duration: 20s;
}
@keyframes move-forever {
  0% {
    transform: translate3d(-90px, 0, 0);
  }
  100% {
    transform: translate3d(85px, 0, 0);
  }
}
/*Shrinking for mobile*/
@media (max-width: 768px) {
  .waves {
    height: 40px;
    min-height: 40px;
  }
  .content {
    height: 30vh;
  }
  h1 {
    font-size: 24px;
  }
}

.font {
  font-family: 'Fredoka One', cursive;
}
</style>
