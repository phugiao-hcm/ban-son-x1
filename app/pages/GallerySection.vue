<template>
    <section class="bg-white py-10 px-4 max-w-[1200px] mx-auto space-y-10">
        <!-- Thương hiệu -->
        <div>
            <h2 class="text-lg font-bold text-green-600 mb-4">Thương hiệu</h2>

            <Swiper
                :modules="[Autoplay]"
                :autoplay="{ delay: 2500 }"
                :breakpoints="{
                    320: { slidesPerView: 2 },
                    640: { slidesPerView: 3 },
                    768: { slidesPerView: 4 },
                    1024: { slidesPerView: 5 },
                }"
                space-between="20"
                loop
            >
                <SwiperSlide
                    v-for="(logo, i) in brandLogos"
                    :key="i"
                    class="flex justify-center"
                >
                    <img :src="logo" alt="logo" class="h-20 object-contain" />
                </SwiperSlide>
            </Swiper>
        </div>

        <!-- Bán chạy -->
        <div>
            <h2 class="text-lg font-bold text-green-600 mb-4">Bán chạy</h2>
            <div
                class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5 gap-4"
            >
                <div
                    v-for="(item, i) in bestSellers"
                    :key="i"
                    class="bg-white rounded shadow-sm p-2 text-center"
                >
                    <img
                        :src="item.image"
                        class="h-28 mx-auto object-contain"
                    />
                    <p class="mt-2 text-sm font-medium line-clamp-2">
                        {{ item.name }}
                    </p>
                    <p class="text-xs text-gray-400">{{ item.sold }} đã bán</p>
                </div>
            </div>
        </div>

        <!-- Top tìm kiếm -->
        <div>
            <h2 class="text-lg font-bold text-green-600 mb-4">Top tìm kiếm</h2>
            <div
                class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5 gap-4"
            >
                <div
                    v-for="(cat, i) in topSearch"
                    :key="i"
                    class="bg-white text-center p-2 rounded shadow-sm"
                >
                    <img :src="cat.image" class="h-24 mx-auto object-contain" />
                    <p class="mt-1 text-sm font-semibold">{{ cat.title }}</p>
                    <p class="text-xs text-gray-400">
                        {{ cat.count }} sản phẩm
                    </p>
                </div>
            </div>
        </div>
    </section>
</template>


<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay } from "swiper/modules";
import "swiper/css";

const brandLogos = [
    "images/brand_1.png",
    "images/brand_2.png",
    "images/brand_3.png",
    "images/brand_4.png",
    "images/brand_5.png",
    "images/brand_6.png",
];

const bestSellers = [
    {
        image: "images/son_1.png",
        name: "Son Tom Ford Màu 05 Front Page",
        sold: "2.4M",
    },
    {
        image: "images/son_2.png",
        name: "Son YSL The Bold 11 Nude Undisclosed",
        sold: "2.43M",
    },
    {
        image: "images/son_3.png",
        name: "Bông tẩy trang",
        sold: "1.94M",
    },
    {
        image: "images/son_4.png",
        name: "Son Kem YSL The Inks Blur 234 Berry Satisfaction",
        sold: "1.6M",
    },
    {
        image: "images/son_5.png",
        name: "Son MAC Ximal Matte 668 Forever Curious",
        sold: "1.41M",
    },
    {
        image: "images/son_6.png",
        name: "Son Dưỡng Dior Addict Lip Maximizer 038 Rose Nude - Mini Size",
        sold: "1.15M",
    },
    {
        image: "images/son_1.png",
        name: "Son Tom Ford Màu 05 Front Page",
        sold: "2.4M",
    },
    {
        image: "images/son_2.png",
        name: "Son YSL The Bold 11 Nude Undisclosed",
        sold: "2.43M",
    },
    {
        image: "images/son_3.png",
        name: "Bông tẩy trang",
        sold: "1.94M",
    },
    {
        image: "images/son_6.png",
        name: "Son Dưỡng Dior Addict Lip Maximizer 038 Rose Nude - Mini Size",
        sold: "1.15M",
    },
];

const topSearch = [
    {
        image: "images/search_1.png",
        title: "Son Đỏ",
        count: 418,
    },
    {
        image: "images/search_2.png",
        title: "Son Lì",
        count: 208,
    },
    {
        image: "images/search_3.png",
        title: "Son dưỡng",
        count: 513,
    },
    {
        image: "images/search_4.png",
        title: "Kem dưỡng da",
        count: 418,
    },
    {
        image: "images/search_5.png",
        title: "Toner",
        count: 201,
    },
];
</script>

<style scoped>
.line-clamp-2 {
    overflow: hidden;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
}
</style>
