<script setup>
import { ref } from 'vue'
</script>

<template>
    <div class="container">
        <div class="section1">
            <div class="text">
                <h1>Agustina Pinto Software developer</h1>
                <!-- <h1>Software Developer</h1> -->
            </div>
        </div>
        <div class="section2">
            <img src="../assets/black-texture.jpg" alt="Black Texture Image">
        </div>
    </div>
</template>

<style scoped>
@font-face {
    font-family: "brastagi";
    src: url(/src/assets/VCR_OSD_MONO_1.001.ttf) format('truetype');
}



.container {
    width: 100vw;
    height: 100vh;
    margin: 0;
    background: black;
    perspective: 1px;
    transform-style: preserve-3d;
    overflow-x: hidden;
    overflow-y: scroll;
}

.section1,
.section2 {
    width: 100%;
    min-height: 100vh;
    position: relative;
    transform-style: preserve-3d;

}

.section1::before {
    content: "";
    width: 100%;
    height: 100%;
    position: absolute;
    left: 0;
    background: url("../assets/parallax-capa1.png") top center;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    transform: translateZ(-1px) scale(2.0);
    filter: blur(2px);
}

.section1::after {
    content: "";
    width: 100%;
    height: 100%;
    position: absolute;
    left: 0;
    background: url("../assets/parallax-capa2.png") top center;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
}

.section1 .text{
    top: 10%;
    transform: translateZ(-0.7px) scale(1.3, 1.3) translate(15%,-10%);
}
.section2 img {
    background: black;
    width: 100%;
    height: auto;
    filter: blur(3px);
}

.text h1 {
    width: 100%;
    top: 20%;
    left: 35%;
    position: absolute;
    font-family: 'brastagi', monospace;
    font-size: 9vw;
    color: rgb(255, 255, 255);
    transform: scale(1, 1.2) translate(-50%, -20%);
    text-shadow: 3px 3px 6px rgb(0, 0, 0);
}
</style>