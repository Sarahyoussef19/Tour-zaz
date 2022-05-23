<template>
    <n-carousel autoplay>
        <img class="carousel-img" src="https://api.lorem.space/image/album?w=1000&h=1500&hash=8B7BCDC2">
        <img class="carousel-img" src="https://api.lorem.space/image/album?w=1000&h=1500&hash=500B67FB">
        <img class="carousel-img" src="https://api.lorem.space/image/album?w=1000&h=1500&hash=9D9539E7">
        <img class="carousel-img" src="https://api.lorem.space/image/album?w=1000&h=1500&hash=B0E33EF4">
        <img class="carousel-img" src="https://api.lorem.space/image/album?w=1000&h=1500&hash=B0E33EF0">
        <img class="carousel-img" src="https://api.lorem.space/image/album?w=1000&h=1500&hash=B0E33EFn">
        <img class="carousel-img" src="https://api.lorem.space/image/album?w=1000&h=1500&hash=B0E33EFw">
        <img class="carousel-img" src="https://api.lorem.space/image/album?w=1000&h=1500&hash=B0E33EF8">
        <img class="carousel-img" src="https://api.lorem.space/image/album?w=1000&h=1500&hash=B0E33EF5">
        <img class="carousel-img" src="https://api.lorem.space/image/album?w=1000&h=1500&hash=B0E33EF8">
    </n-carousel>
</template>
<script>
import { NCarousel } from "naive-ui";
export default {
    components: { NCarousel }
}
</script>
<style>
.carousel-img {
    width: 100%;
    height: 240px;
    object-fit: cover;
}
</style>