<script setup>
import { ref } from 'vue'

</script>

<template>
  <div class="banner">
    <img class="banner-pic" src="../assets/banner.jpg">

    <div class="slider">
      <div class="slide-track">
        <div class="slide">
          <h1>Agustina Pinto</h1>
        </div>
      </div>
      <div class="slide-track">
        <div class="slide">
          <h1>Software Developer</h1>
        </div>
      </div>
    </div>

    <div class="cv-pic">
      <div class="content">
        <img class="my-pic" src="../assets/cv-picture-2-bw.jpg">
        <a class="link" href="https://www.linkedin.com/in/agustina-pinto-">Contact me</a>
      </div>
    </div>
  </div>
</template>

<style scoped>
@font-face {
  font-family: "brastagi";
  src: url(/src/assets/VCR_OSD_MONO_1.001.ttf) format('truetype');
}

.banner {
  max-width: 100%;
  max-height: 47rem;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: rgb(9, 9, 9);
  overflow: hidden;
  position: sticky;
  top: 0;
}

.banner .banner-pic {
  opacity: 0.6;
  width: 100%;
}

.slider {
  width: 100%;
  height: auto;
  margin: auto;
  overflow: hidden;
  position: absolute;
  top: 0;
}

.slider .slide-track {
  display: flex;
  flex-direction: row;
  animation: scroll 10s linear infinite;
  -webkit-animation: scroll 20s linear infinite;
  width: calc(200px * 20);
}

.slider .slide {
  width: 100%;
}

.slider .slide h1 {
  width: auto;
  margin: 0;
  font-family: "brastagi", monospace;
  font-size: 10rem;
  color: aliceblue;
}

@keyframes scroll {
  0% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
  }
  100% {
    -webkit-transform: translateX(calc(-200px * 10));
    transform: translateX(calc(-200px * 15));
  }
}

.cv-pic {
  position: absolute;
  bottom: 2rem;
  background-color: rgba(0, 0, 0, 0.82);
  width: 360px;
  height: 360px;
  border-radius: 50%;
  overflow: hidden;
}

.cv-pic::before {
  content: '';
  position: absolute;
  inset: -10px 145px;
  background: linear-gradient(315deg, rgb(52, 67, 200), rgb(108, 35, 96));
  transition: 0.5s;
  animation: animate 4s linear infinite;
  overflow: hidden;
}

.cv-pic:hover::before {
  inset: -20px 0px;
}

@keyframes animate {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(360deg);
  }
}

.cv-pic::after {
  content: '';
  position: absolute;
  inset: 10px;
  background: rgb(0, 0, 0);
  border-radius: 50%;
  z-index: 1;
}

.content {
  position: absolute;
  inset: 30px;
  border: 6px solid rgba(255, 255, 255, 0.687);
  z-index: 3;
  border-radius: 50%;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.content img {
  position: absolute;
  left: 0;
  right: 0;
  min-width: 100%;
  height: 100%;
  object-fit: cover;
  transition: 0.5s;
  pointer-events: none;
  z-index: 3;
}

.cv-pic:hover .content img {
  opacity: 0.2;
}

.content a {
  position: relative;
  padding: 1rem;
  color: black;
  background: rgb(255, 255, 255);
  border-radius: 30px;
  transition: 0.5s;
  text-decoration: none;
}

.content a:hover {
  letter-spacing: 3px;
}
</style>
