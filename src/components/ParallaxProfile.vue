<script setup>
import { ref, onMounted, onUpdated } from 'vue'
import ExpTimeline from '../components/ExperienceTimeline.vue'
import ExpEduc from '../components/Experience-Education.vue'

const canvasRef = ref(null)

onMounted(() => {
    particlesJS("particles-js", {
        "particles": {
            "number": {
                "value": 50,
                "density": {
                    "enable": true,
                    "value_area": 800
                }
            },
            "color": {
                "value": "#ffffff"
            },
            "shape": {
                "type": "circle",
                "stroke": {
                    "width": 0,
                    "color": "#000000"
                },
            },
            "opacity": {
                "value": 0.5,
                "random": true,
                "anim": {
                    "enable": true,
                    "speed": 1,
                    "opacity_min": 0,
                    "sync": false
                }
            },
            "size": {
                "value": 1  // Ajusté el tamaño de las partículas a 2
            },
            "move": {
                "enable": true,
                "speed": 2,
                "direction": "none",
                "random": false,
                "straight": false,
                "out_mode": "out",
                "bounce": false,
            }
        }
    });
});
</script>


<template>
    <div class="container">
        <div class="section1">
            <div class="text">
                <h1>Agustina Pinto Software developer</h1>
            </div>
        </div>
        <div class="section2" >
            <div >
                <div class="title-container">
                    <span class="skills-title" ref="skillsTitle" @animationiteration="restartAnimation">Experience</span>
                </div>
                <div class="exp-info" >
                        <ExpEduc />
                    <!-- <ExpTimeline /> -->
                </div>
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
    background: rgb(2, 1, 20);
    perspective: 1px;
    transform-style: preserve-3d;
    overflow-x: hidden;
    overflow-y: scroll;
}

.section2 {
    position: absolute;
    z-index: 1;
    width: 100%;
    /* Asegúrate de que la sección 2 ocupe toda la pantalla */
    background: rgb(2, 1, 20);
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
    border-radius: 15%;
    text-shadow: 3px 2px 5px rgb(0, 0, 0);
    top: 10%;
    left: 2%;
    color: rgba(255, 255, 255, 0.879);
    background: rgba(128, 128, 128, 0.608);
    font-size: 2.5rem;
    display: block;
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    white-space: nowrap;
    border-right: 4px solid;
    width: 10ch;
    animation: typing 4s steps(10) infinite, blink .3s infinite step-end alternate;
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
    color: rgb(255, 255, 255);
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
        animation: none;
    }

    .title-container {
        position: absolute;
        top: 5.6%;
        left: 18%;
        margin-top: 2%;
    }
}
</style>