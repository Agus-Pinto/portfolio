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
            <div>
                <div class="title-container">
                    <span class="skills-title" ref="skillsTitle" @animationiteration="restartAnimation">Skills</span>
                </div>
            </div>
            <div class="skills-info">
                <tr>
                    <td>React</td>
                    <td>CSS</td>
                    <td>HTML</td>
                    <td>Javascript</td>
                    <td>Typescript</td>
                </tr>
                <h2 class="content">React</h2>
                <h2 class="content">CSS</h2>
                <h2 class="content">HTML</h2>
                <h2 class="content">Javascript</h2>
                <h2 class="content">Typescript</h2>
            </div>
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

.section1 .text {
    top: 10%;
    transform: translateZ(-0.7px) scale(1.3, 1.3) translate(15%, -10%);
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

.title-container {
    display: flex;
    width: 100vw;
    justify-content: center;
    align-items: center;
}

.skills-title {
    position: absolute;
    text-shadow: 3px 3px 6px rgb(0, 0, 0);
    top: 20%;
    color: aliceblue;
    background-color: crimson;
    font-size: 5rem;
    display: block;
    font-family: 'brastagi', monospace;
    white-space: nowrap;
    border-right: 4px solid;
    width: 7ch;
    animation: typing 4s steps(7) infinite, blink .3s infinite step-end alternate;
    overflow: hidden;
}

@keyframes typing {
    from {
        width: 0;
    }
}

@keyframes blink {
    50% {
        border-color: transparent;
    }
}

.skills-info {
    width: 100vw;
    position: absolute;
    top: 40%;
    color: aliceblue;
}

.content {
    max-width: 100vw;
    position: relative;
    margin-bottom: 1rem;
    padding-bottom: 3.5rem;
    font-family: 'brastagi', monospace;
    font-size: 2.5em;
    transition: 0.5s;
    transform-origin: left;
    transform: scaleX(1);
}

.skills-info .content::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    max-width: 100vw;
    height: 100%;
    background: rgb(0, 162, 255);
}
</style>