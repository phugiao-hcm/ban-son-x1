<template>
    <section class="bg-white">
        <!-- Wrapper giới hạn chiều rộng và căn giữa -->
        <div class="max-w-6xl mx-auto px-4 py-6">
            <!-- Danh sách icon menu -->
            <div
                class="grid grid-cols-3 sm:grid-cols-4 md:grid-cols-6 lg:grid-cols-6 gap-4 text-center"
            >
                <div
                    v-for="(item, i) in menus"
                    :key="i"
                    class="flex flex-col items-center justify-center text-sm"
                >
                    <img
                        :src="item.icon"
                        class="w-12 h-12 object-contain mb-1"
                        :alt="item.label"
                    />
                    <span class="text-gray-700 leading-snug text-center">{{
                        item.label
                    }}</span>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
const menus = [
    { icon: "images/service_1.png", label: "Beauty Week" },
    { icon: "images/service_2.png", label: "Giao 2H" },
    { icon: "images/service_3.png", label: "Nước Hoa Chính Hãng" },
    { icon: "images/service_4.png", label: "Clinic & S.P.A" },
    { icon: "images/service_5.png", label: "Clinic Deals" },
    { icon: "images/service_6.png", label: "Mua Là Có Quà" },
];
</script>
