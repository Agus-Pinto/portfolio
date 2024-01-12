<script setup>
import { ref } from 'vue'
</script>

<template>
  <div class="img-container">
    <img src="../assets/black-texture.jpg" alt="Black Texture Image">
  </div>
</template>

<style scoped>
.img-container {
  background: black;
  width: 100%;
  position: relative;
}

.img-container img {
  width: 100%;
  height: auto;
  display: block;
}

</style>
