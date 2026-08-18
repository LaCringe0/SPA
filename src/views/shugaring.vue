<template>
    <section class="px-5 sm:px-8 lg:px-16 xl:px-[120px] py-16 relative flex flex-col items-center">
        <h4 class="text-white text-3xl sm:text-4xl font-bold font-abhaya text-center">Shugaring</h4>
        <h5 class="max-w-[995px] text-white/90 text-lg sm:text-xl font-normal font-crimson leading-relaxed text-center mt-4">Discover gentle care and perfectly smooth skin with our professional sugaring. Our experienced specialists use only high-quality sugar pastes crafted with love for your comfort. Forget about unpleasant sensations - our sugaring ensures efficient hair removal while maintaining the utmost respect for your skin. Treat yourself to smoothness and pleasure with our professional sugaring, where beauty is in every detail.</h5>
        <img src="@/assets/shugaring.png" alt="Sugaring treatment" class="w-full max-w-[995px] h-auto mt-8 rounded-2xl shadow-2xl">
        <button @click="modalState?.open()" class="border-2 md:border-4 border-white px-12 sm:px-[79px] py-4 sm:py-[22px] transition-all hover:text-black hover:bg-white duration-300 scale-100 translate-y-0 hover:scale-105 active:scale-95 cursor-pointer text-white text-2xl sm:text-4xl font-extrabold font-abhaya mt-9 sm:mt-11">
            Reserve
        </button>
    </section>
</template>

<script setup lang="js">
import { inject } from 'vue'

const modalState = inject('modalState')
</script>
