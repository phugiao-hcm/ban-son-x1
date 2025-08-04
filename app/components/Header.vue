<template>
    <header class="bg-pink-100 sticky top-0 z-50 shadow">
        <div
            class="container mx-auto px-4 py-3 flex justify-between items-center"
        >
            <!-- Logo -->
            <NuxtLink to="/" class="text-2xl font-bold text-pink-600">
                SonMôi<span class="text-pink-400">Xinh</span>
            </NuxtLink>

            <!-- Desktop menu -->
            <nav
                class="hidden md:flex space-x-6 text-sm font-medium text-pink-700"
            >
                <NuxtLink to="/" class="hover:text-pink-500"
                    >Trang chủ</NuxtLink
                >
                <NuxtLink to="/" class="hover:text-pink-500">Sản phẩm</NuxtLink>
                <NuxtLink to="/" class="hover:text-pink-500"
                    >Thương hiệu</NuxtLink
                >
                <NuxtLink to="/" class="hover:text-pink-500"
                    >Blog làm đẹp</NuxtLink
                >
                <NuxtLink to="/" class="hover:text-pink-500">Liên hệ</NuxtLink>
            </nav>

            <!-- Mobile toggle -->
            <button
                @click="menuOpen = !menuOpen"
                class="md:hidden text-pink-600"
                aria-label="Toggle menu"
            >
                <svg
                    v-if="!menuOpen"
                    xmlns="http://www.w3.org/2000/svg"
                    class="h-6 w-6"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                >
                    <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M4 6h16M4 12h16M4 18h16"
                    />
                </svg>
                <svg
                    v-else
                    xmlns="http://www.w3.org/2000/svg"
                    class="h-6 w-6"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                >
                    <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M6 18L18 6M6 6l12 12"
                    />
                </svg>
            </button>
        </div>

        <!-- Mobile menu -->
        <div
            v-if="menuOpen"
            class="md:hidden bg-pink-50 px-4 pb-4 animate-fade-down"
        >
            <NuxtLink
                to="/"
                class="block py-1 text-pink-700 hover:text-pink-500"
                >Trang chủ</NuxtLink
            >
            <NuxtLink
                to="/"
                class="block py-1 text-pink-700 hover:text-pink-500"
                >Sản phẩm</NuxtLink
            >
            <NuxtLink
                to="/"
                class="block py-1 text-pink-700 hover:text-pink-500"
                >Thương hiệu</NuxtLink
            >
            <NuxtLink
                to="/"
                class="block py-1 text-pink-700 hover:text-pink-500"
                >Blog làm đẹp</NuxtLink
            >
            <NuxtLink
                to="/"
                class="block py-1 text-pink-700 hover:text-pink-500"
                >Liên hệ</NuxtLink
            >
        </div>
    </header>
</template>

<script setup>
import { ref } from "vue";
const menuOpen = ref(false);
</script>

<style scoped>
@keyframes fade-down {
    0% {
        opacity: 0;
        transform: translateY(-10px);
    }
    100% {
        opacity: 1;
        transform: translateY(0);
    }
}
.animate-fade-down {
    animation: fade-down 0.2s ease-out;
}
</style>
