<template>
    <div class="cont-jumb position-relative">
        <img src="../assets/images/slider-1-bg.jpg" alt="">
        <h2>CONFERENCE ON</h2>
        <h1>SOCIAL NETWORKS</h1>
        <img class="position-absolute" src="../assets/images/1-item-2.jpg" alt="">
    </div>
</template>

<script>
export default {

}
</script>

<style lang='scss' scoped>
.cont-jumb {
        height: 36rem;
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
        text-shadow: 0 0 10px #000;
    }
    h1 {
        position: absolute;
        top: 45%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 5rem;
        font-weight: bold;
        color: #fff;
        text-shadow: 0 0 10px #000;
    }
</style>