<script setup>
import { ref } from 'vue'
</script>

<template>
    <div class="box-container">
        <div class="timeline">
            <div class="container left-container">
                <div class="image-container">
                    <img src="../assets/bbs.ico">
                </div>
                <div class="text-box">
                    <h2>Software Developer</h2>
                    <small>x - x</small>
                    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sit, reiciendis. Sunt numquam, officia
                        architecto aperiam inventore ipsum eligendi est rem totam voluptatibus nam placeat, perferendis
                        nulla odio velit animi voluptate.</p>
                    <span class="left-container-arrow"></span>
                </div>
            </div>

            <div class="container right-container">
                <img src="../assets/bbs.ico">
                <div class="text-box">
                    <h2>Software Developer</h2>
                    <small>2020 - 2021</small>
                    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sit, reiciendis. Sunt numquam, officia
                        architecto aperiam inventore ipsum eligendi est rem totam voluptatibus nam placeat, perferendis
                        nulla odio velit animi voluptate.</p>
                    <span class="right-container-arrow"></span>
                </div>
            </div>

            <div class="container left-container">
                <img src="../assets/bbs.ico">
                <div class="text-box">
                    <h2>Software Developer</h2>
                    <small>x - x</small>
                    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sit, reiciendis. Sunt numquam, officia
                        architecto aperiam inventore ipsum eligendi est rem totam voluptatibus nam placeat, perferendis
                        nulla odio velit animi voluptate.</p>
                    <span class="left-container-arrow"></span>
                </div>
            </div>

            <div class="container right-container">
                <img src="../assets/bbs.ico">
                <div class="text-box">
                    <h2>Software Developer</h2>
                    <small>x - x</small>
                    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sit, reiciendis. Sunt numquam, officia
                        architecto aperiam inventore ipsum eligendi est rem totam voluptatibus nam placeat, perferendis
                        nulla odio velit animi voluptate.</p>
                    <span class="right-container-arrow"></span>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.box-container {
    display: flex;
    justify-content: center;
}

.text-box {
    color: aliceblue;
    padding: 5px 30px;
    background: rgb(91, 127, 194);
    position: relative;
    border-radius: 6px;
    font-size: 15px;
    text-shadow: 3px 3px 5px rgb(32, 32, 32);
    text-align: left;
}

.timeline {
    position: relative;
    max-width: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;
    margin: 100px auto;
}

.container {
    max-width: 40%;
    padding: 10px 30px;
    position: relative;
    animation: movedown 1s linear forwards;
    opacity: 0;
}


@keyframes movedown {
    0% {
        opacity: 1;
        transform: translateY(-30px);
    }

    100% {
        opacity: 1;
        transform: translateY(0px);
    }
}

.container:nth-child(1) {
    animation-delay: 0s;
}

.container:nth-child(2) {
    animation-delay: 1s;
}

.container:nth-child(3) {
    animation-delay: 2s;
}

.container:nth-child(4) {
    animation-delay: 3s;
}

.left-container {
    right: -3.5%;
}

.right-container {
    left: 52.5%;
}

.container img , .image-container img{
    position: absolute;
    width: 40px;
    border-radius: 50%;
    background: rgb(255, 255, 255);
    padding: 2px;
    top: 32px;
}

.left-container img {
    right: -9%;
}

.right-container img {
    left: -9%;
}

.timeline::after {
    content: "";
    position: absolute;
    width: 6px;
    height: 100%;
    background: white;
    top: 0;
    left: 50%;
    z-index: 1;
    animation: moveline 6s linear forwards;
}

@keyframes moveline {
    0% {
        height: 0%;
    }

    100% {
        height: 100%;
    }
}

.text-box h2 {
    font-weight: 800;
}

.text-box small {
    display: inline-block;
    position: relative;
}

.left-container-arrow {
    height: 0;
    width: 0;
    position: absolute;
    top: 28px;
    z-index: 1;
    border-top: 15px solid transparent;
    border-bottom: 15px solid transparent;
    border-left: 15px solid rgb(91, 127, 194);
    right: -14px;
}

.right-container-arrow {
    height: 0;
    width: 0;
    position: absolute;
    top: 28px;
    z-index: 1;
    border-top: 15px solid transparent;
    border-bottom: 15px solid transparent;
    border-right: 15px solid rgb(91, 127, 194);
    left: -14px;
}

@media screen and (max-width: 625px) {
    .left-container {
        right: -0%;
    }
    
    .right-container {
        left: 52%;
    }
}

@media screen and (max-width: 600px) {
    .timeline {
        margin: 50px auto;
    }

    .timeline::after{
        left: 30px;
        z-index: 1;
    }

    .container {
        max-width: 100%;
        padding-left: 80px;
        padding-right: 25px;
    }

    .text-box {
        font-size: 1.2rem;
    }

    .text-box small {
        margin-bottom: 5px;
    }

    .right-container, .left-container {
        left: 0%;
    }

    .left-container img, .right-container img {
        left: 10px;
        z-index: 10;
    }

    .left-container-arrow , .right-container-arrow {
        border-right: 15px solid rgb(91, 127, 194);
        border-left: 0;
        left: -4%;
    }
}

</style>
