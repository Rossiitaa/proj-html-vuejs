<template>
    <div class="cont-jumb position-relative">
        <img src="../assets/images/slider-1-bg.jpg" alt="">
        <h2>CONFERENCE ON</h2>
        <h1>SOCIAL NETWORKS</h1>
        <img class="line" src="../assets/images/1-item-2.jpg" alt="">
        <p class="">23-26 MAY 2019 <span class="mx-4 fw-light">/</span> SANS FRANCISCO <span class="mx-4 fw-light">/</span> 8 SPEAKERS</p>
        <button class="btn">REGISTER ONLINE</button>
    </div>
</template>

<script>
export default {

}
</script>

<style lang='scss' scoped>
.cont-jumb {
        height: 40rem;
    }

img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    }

    h2 {
        position: absolute;
        top: 25%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 4rem;
        font-weight: lighter;
        color: #fff;
    }
    h1 {
        position: absolute;
        top: 40%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 6rem;
        font-weight: bold;
        color: #fff;
    }
    img.line {
        position: absolute;
        top: 58%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 35rem;
        height: 0.3rem;
    }
    p {
        position: absolute;
        top: 62%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 1.2rem;
        font-weight: bold;
        color: #fff;
    }
    button {
        position: absolute;
        top: 75%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 1.2rem;
        font-weight: bold;
        color: #fff;
        padding: 1rem 2rem;
        background-color: #f72a0c;

        &:hover {
            background-color: #f72a0c;
            color: #fff;
        }
    }
</style>