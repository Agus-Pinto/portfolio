<script setup>
import { ref } from 'vue'
import ExpTimeline from '../components/ExperienceTimeline.vue'
import ExpEduc from '../components/Experience-Education.vue'
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
                    <span class="skills-title" ref="skillsTitle" @animationiteration="restartAnimation">Experience</span>
                </div>
            </div>
            <div class="exp-info">
                <!-- <ExpTimeline /> -->
                <ExpEduc />
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
    width: 100vw;
    height: 100vh;
    filter: blur(10px);
    border: none;
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
    justify-content: left;
    align-items: left;
}

.skills-title {
    position: absolute;
    padding: 5px;
    text-shadow: 3px 3px 6px rgb(0, 0, 0);
    top: 10%;
    left: 2%;
    color: aliceblue;
    background-color: rgb(75, 109, 173);
    font-size: 2.5rem;
    display: block;
    font-family: 'brastagi', monospace;
    white-space: nowrap;
    border-right: 4px solid;
    width: 11ch;
    animation: typing 4s steps(11) infinite, blink .3s infinite step-end alternate;
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

.exp-info {
    position: absolute;
    top: 15%;
    padding: 0%;
    margin: 0 auto;
}

@media only screen and (max-width: 600px) {
    .text h1 {
        font-size: 15vw;
        width: 100%;
    }

    .skills-title {
        font-size: 2.5em;
    }

    .title-container {
        position: absolute;
        top: 5.5%;
        left: 20%;
    }
}
</style>