<script setup>
import { ref } from 'vue'
</script>

<template>
    <div class="exp-container">
        <div class="exp-box exp-box1">
            <div class="exp-img"><img src="../assets/logo.png" alt="Software Developer"></div>
            <div class="exp-content">
                <div class="exp-title"><h1>Software Developer</h1></div>
                <div class="exp-date"><h2>x - x</h2></div>
                <div class="exp-text"><p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga iure nesciunt neque numquam totam mollitia et consectetur, repudiandae saepe consequatur ipsam beatae nemo rem non delectus aliquam cupiditate laudantium sapiente?</p></div>
            </div>
        </div>
        <div class="exp-box exp-box2">
            <div class="exp-img"><img src="../assets/logo.png" alt="Trainee"></div>
            <div class="exp-content">
                <div class="exp-title"><h1>Trainee</h1></div>
                <div class="exp-date"><h2>x - x</h2></div>
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
    width: 80%; /* Ajusta el ancho del contenedor principal según sea necesario */
    margin-top: 5.5%; /* Centra el contenedor en la página */
    margin-left: 10%;
}

.exp-box {
    display: grid;
    grid-template-columns: 20% 1fr; /* Ajusta el tamaño de la primera columna según sea necesario */
    gap: 10px;
    align-items: center;
    background: rgba(128, 128, 128, 0.532);
    text-align: center;
}

.exp-img {
    background: white;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
}

.exp-img img {
    max-width: 80%; /* Asegura que la imagen no se salga de su contenedor */
    max-height: 100%; /* Ajusta la altura máxima de la imagen */
}

.exp-content {
    padding: 10px; /* Añade un relleno interno según sea necesario */
}

</style>
