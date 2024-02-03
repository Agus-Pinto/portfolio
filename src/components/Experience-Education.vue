<script setup>
import { ref } from 'vue'
</script>

<template>
    <div class="exp-container">
        <div class="exp-box exp-box1">
            <div class="exp-img"><img src="../assets/logo.png" alt="Software Developer"></div>
            <div class="exp-content">
                <div class="exp-title">
                    <h1>Software Developer</h1>
                </div>
                <div class="exp-date">
                    <h2>August 2021 - February 2024</h2>
                </div>
                <div class="exp-text">
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga iure nesciunt neque numquam totam
                        mollitia et consectetur, repudiandae saepe consequatur ipsam beatae nemo rem non delectus aliquam
                        cupiditate laudantium sapiente?</p>
                </div>
                <div class="tech-icons">
                    <img src="../assets/react.webp" alt="">
                    <img src="../assets/react.webp" alt="">
                    <img src="../assets/react.webp" alt="">
                    <img src="../assets/react.webp" alt="">
                </div>
            </div>
        </div>
        <div class="exp-box exp-box2">
            <div class="exp-img"><img src="../assets/logo.png" alt="Trainee"></div>
            <div class="exp-content">
                <div class="exp-title">
                    <h1>Trainee</h1>
                </div>
                <div class="exp-date">
                    <h2>September 2020 - August 2021</h2>
                </div>
                <div class="exp-text">
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga iure nesciunt neque numquam totam
                        mollitia et consectetur, repudiandae saepe consequatur ipsam beatae nemo rem non delectus aliquam
                        cupiditate laudantium sapiente?</p>
                </div>
                <div class="tech-icons">
                    <img src="../assets/react.png" alt="">
                    <img src="../assets/html.png" alt="">
                    <img src="../assets/css.png" alt="">
                    <img src="../assets/materialUi.png" alt="">
                    <img src="../assets/python.png" alt="">
                    <img src="../assets/docker.png" alt="">
                    <img src="../assets/aws.png" alt="">
                    <img src="../assets/github.png" alt="">
                </div>
            </div>
        </div>
    </div>
    <div class="title-container">
        <span class="educ-title" ref="skillsTitle" @animationiteration="restartAnimation">Education</span>
    </div>

    <div class="educ-container">
        <div class="edc-box">
            <div class="edc-img"><img src="../assets/logo-issd.svg" alt="Trainee"></div>
            <div class="edc-content">
                <div class="edc-title">
                    <h1>Systems analyst technician</h1>
                </div>
                <div class="edc-date">
                    <h2>January 2020 - In progress</h2>
                </div>
                <div class="edc-text">
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga iure nesciunt neque numquam totam
                        mollitia et consectetur, repudiandae saepe consequatur ipsam beatae nemo rem non delectus aliquam
                        cupiditate laudantium sapiente?</p>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.exp-container h1,
h2,
p,
.educ-container h1,
h2,
p {
    color: wheat;
}


.exp-container,
.educ-container {
    display: grid;
    grid-template-columns: 1fr;
    gap: 20px;
    width: 70%;
    margin-top: 5.5%;
    margin-left: 15%;
}

.educ-container {
    margin-top: 12%;
    padding-bottom: 5%;
}

.exp-box,
.edc-box {
    display: grid;
    grid-template-columns: 20% 1fr;
    /* Ajusta el tamaño de la primera columna según sea necesario */
    gap: 10px;
    align-items: center;
    background: rgba(128, 128, 128, 0.474);
    text-align: center;
}

.exp-box {
    margin-bottom: 2%;
}

.tech-icons {
    display: flex;
    justify-content: center;
    padding-top: 2%;
}

.tech-icons img {
    padding-right: 2%;
    width: 30px;
    background: white;
    border-radius: 100%;
    padding: 1.2%;
    margin-left: 2%;
}

.exp-box:hover {
    box-shadow: -1px 0px 9px 2px rgb(86, 90, 94);

}

.exp-img,
.edc-img {
    background: rgba(255, 255, 255, 0.426);
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
    border-right: 3px solid rgba(38, 38, 38, 0.813);
}

.exp-img img,
.edc-img img {
    max-width: 80%;
    max-height: 100%;
    opacity: 1;
}

.exp-content,
.edc-content {
    padding: 10px;
    margin-top: -1%;
    margin-bottom: 2%;
}

.exp-title,
.edc-title {
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}

.exp-date,
.edc-date {
    border-bottom: 2px solid rgb(55, 55, 55);
    margin-right: 5%;
    margin-left: 5%;
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-size: xx-small;
}

.title-container {
    display: flex;
    width: 100vw;
    justify-content: left;
    align-items: left;
}

.educ-title {
    position: absolute;
    padding: 5px;
    text-shadow: 3px 2px 5px rgb(0, 0, 0);
    margin-top: 5%;
    left: 2%;
    color: rgba(255, 255, 255, 0.879);
    background-color: rgba(255, 255, 255, 0.341);
    font-size: 2.5rem;
    display: block;
    font-family: 'brastagi', monospace;
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

@media only screen and (max-width: 600px) {

    .exp-container,
    .educ-container {
        width: 90%;
        margin-left: 5%;
    }

    .educ-container {
        margin-top: 50%;
    }

    .educ-title {
        animation: none;
        font-size: 2.5em;
    }

    .title-container {
        position: absolute;
        left: 20%;
        margin-top: 15%;
    }

    .tech-icons {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }

    .tech-icons img {
        margin: 5px;
        width: 11%;
    }
}
</style>
