<template>
    <div class="">
        <section class="bg-main md:pt-20 pt-28">
            <div class="container-xl mx-auto flex flex-col justify-center items-center md:py-20">
                <h1 class="md:text-[7.5vw] text-[2.5em] inline-flex items-center serif italic leading-[95%]">
                    Revolutionize
                    <span class="flex items-centeer md:ms-4">
                        <img src="https://via.placeholder.com/50"
                            class="md:w-[100px] rounded-full border-[2px] border-[#0c3bb8] md:h-[100px]" alt="">
                        <img src="https://via.placeholder.com/50"
                            class="md:w-[100px] rounded-full border-[2px] -ms-6 border-[#0c3bb8] md:h-[100px]" alt="">
                        <img src="https://via.placeholder.com/50"
                            class="md:w-[100px] rounded-full border-[2px] -ms-6 border-[#0c3bb8] md:h-[100px]" alt="">
                    </span>
                </h1>
                <h1 class="md:text-[7.5vw] text-[2.5em] font-[300] inline-flex archivo leading-[95%]">the way to&nbsp;
                    <span class="font-bold archivo">&lt;build/&gt;</span>
                </h1>
                <h1 class="md:text-[7.5vw] text-[2.5em] font-[600] inline-flex leading-[95%]">every&nbsp;
                    <span class="italic font-normal serif">think.</span>
                </h1>
                <button class="mt-[5em] border  md:py-2 md:px-4 rounded-full">Start Journey</button>
            </div>
        </section>
        <section class="bg-main">
            <div
                class="container-xl bg-[url('background.png')] bg-contain bg-no-repeat bg-center mx-auto flex flex-col justify-center h-dvh items-center md:py-20 md:px-[10em]">
                <div class="relative">
                    <img :src="image" class="w-[30vw]" alt="">
                    <div class="absolute top-10 w-full h-full flex flex-col items-center justify-end">
                        <div class="flex">
                            <button v-for="(btn, index) in buttons" :key="index"
                                :class="['px-4 py-2', activeButton === btn.type ? 'bg-blue-400' : 'bg-gray-200']"
                                @click="changeImage(btn.type)">
                                {{ btn.label }}
                            </button>
                        </div>
                        <h1 class="text-[3.8vw] leading-[90%] font-[600] text-center">Meet with <br>
                            <span class="serif italic">Agis.</span>
                        </h1>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
export default {
    data() {
        return {
            image: '/agis.png', // Default image
            activeButton: 'surf',
            buttons: [
                { label: 'Surf', type: 'surf', image: '/agis.png' },
                { label: 'Skate', type: 'skate', image: '/arrow.gif' }
            ]
        }
    },
    methods: {
        changeImage(type) {
            const selectedButton = this.buttons.find(btn => btn.type === type);
            this.image = selectedButton.image;
            this.activeButton = type;
        }
    }
}
</script>

<style lang="scss" scoped></style>