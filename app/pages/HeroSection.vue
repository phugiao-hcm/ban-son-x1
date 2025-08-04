<template>
    <section class="relative">
        <Swiper
            :modules="[Autoplay]"
            :autoplay="{ delay: 4000 }"
            loop
            class="w-full h-[20vh] sm:h-[30vh] md:h-[65vh]"
        >
            <SwiperSlide v-for="(slide, i) in slides" :key="i">
                <div
                    class="relative w-full h-full bg-cover bg-center"
                    :style="{ backgroundImage: `url(${slide.image})` }"
                >
                    <!-- Overlay -->
                    <!-- <div class="absolute inset-0 bg-black/30"></div>
                    <div
                        class="absolute inset-0 flex flex-col justify-center items-center text-center text-white px-4"
                    >
                        <h2
                            class="text-3xl md:text-5xl font-bold mb-3 drop-shadow-md"
                        >
                            {{ slide.title }}
                        </h2>
                        <p class="text-lg md:text-xl drop-shadow-sm">
                            {{ slide.subtitle }}
                        </p>
                        <NuxtLink
                            to="/products"
                            class="mt-6 inline-block bg-pink-500 hover:bg-pink-600 text-white font-medium px-6 py-3 rounded shadow transition"
                        >
                            Mua ngay
                        </NuxtLink>
                    </div> -->
                </div>
            </SwiperSlide>
        </Swiper>
    </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay } from "swiper/modules";
import "swiper/css";

const slides = [
    {
        image: "images/hero_1.png",
        title: "Khám phá Bộ sưu tập Son Mới",
        subtitle: "Sắc màu thời thượng – Tự tin toả sáng mỗi ngày",
    },
    {
        image: "images/hero_2.png",
        title: "Son lì cao cấp từ Hàn Quốc",
        subtitle: "Mịn môi – Lên màu chuẩn – Lâu trôi cả ngày",
    },
    {
        image: "images/hero_3.png",
        title: "Ưu đãi Đặc biệt trong tuần",
        subtitle: "Giảm giá đến 50% cho đơn hàng từ 499K",
    },
];
</script>

<style scoped>
/* Custom styles if needed */
</style>
