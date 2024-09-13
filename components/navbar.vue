<template>
    <div>
        <header class="fixed w-full pt-6 md:px-[10em]">
            <div
                class="sm:px-12 mx-auto transition-opacity duration-500 flex items-center rounded-2xl backdrop-blur-lg justify-between p-4 shadow-xl bg-white">
                <div class="flex items-center space-x-2">
                    <button>
                        <img src="https://cdn-icons-png.flaticon.com/128/3845/3845868.png" alt="Logo" class="w-10">
                    </button>
                </div>
                <nav class="flex items-center space-x-1 text-sm font-medium text-gray-800">
                    <button class="rounded bg-red-600 px-3 py-2 text-white transition hover:bg-red-700"> Sign Up
                    </button>
                </nav>
            </div>
        </header>
    </div>
</template>

<script>
import { ref, onMounted, onUnmounted } from 'vue';

export default {
    setup() {

    }
};
</script>

<style scoped>
#header {
    transition: opacity 10s ease-in-out !important;
}
</style>
