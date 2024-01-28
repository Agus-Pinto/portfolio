<script setup>
import { ref } from 'vue'
</script>

<template>
    <div class="exp-container">
        <div class="exp-box exp-box1">
            <div class="exp-img"><img src="../assets/logo.png" alt="Software Developer"></div>
            <div class="exp-content">
                <div class="exp-title"><h1>Software Developer</h1></div>
                <div class="exp-date"><h2>August 2021 - February 2024</h2></div>
                <div class="exp-text"><p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga iure nesciunt neque numquam totam mollitia et consectetur, repudiandae saepe consequatur ipsam beatae nemo rem non delectus aliquam cupiditate laudantium sapiente?</p></div>
            </div>
        </div>
        <div class="exp-box exp-box2">
            <div class="exp-img"><img src="../assets/logo.png" alt="Trainee"></div>
            <div class="exp-content">
                <div class="exp-title"><h1>Trainee</h1></div>
                <div class="exp-date"><h2>September 2020 - August 2021</h2></div>
                <div class="exp-text"><p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga iure nesciunt neque numquam totam mollitia et consectetur, repudiandae saepe consequatur ipsam beatae nemo rem non delectus aliquam cupiditate laudantium sapiente?</p></div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.exp-container h1, h2, p {
    color: wheat;
}

.exp-container {
    display: grid;
    grid-template-columns: 1fr;
    gap: 20px;
    width: 70%; /* Ajusta el ancho del contenedor principal según sea necesario */
    margin-top: 5.5%; /* Centra el contenedor en la página */
    margin-left: 15%;
}

.exp-box {
    display: grid;
    grid-template-columns: 20% 1fr; /* Ajusta el tamaño de la primera columna según sea necesario */
    gap: 10px;
    align-items: center;
    background: rgba(128, 128, 128, 0.286);
    text-align: center;
}

.exp-img {
    background: rgba(255, 255, 255, 0.238);
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
    border-right: 3px solid rgba(38, 38, 38, 0.813);
}

.exp-img img {
    max-width: 80%;
    max-height: 100%;
    opacity: 1;
}

.exp-content {
    padding: 10px;
    margin-top: -2%;
    margin-bottom: 2%;
}

.exp-title {
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}

.exp-date {
    border-bottom: 2px solid rgb(55, 55, 55);
    margin-right: 5%;
    margin-left: 5%;
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-size: xx-small;
}

</style>
