<template>
    <section class="px-5 sm:px-8 lg:px-16 xl:px-[120px] py-16 relative flex flex-col items-center">
        <h4 class="text-white text-3xl sm:text-4xl font-bold font-abhaya text-center">Bathhouse</h4>
        <h5 class="max-w-[995px] text-white/90 text-lg sm:text-xl font-normal font-crimson leading-relaxed text-center mt-4">Immerse yourself in the world of true bliss with our sauna. Our cozy rooms are filled with warmth and a relaxing atmosphere. Feel the surge of energy in the steam room, refresh your body in the cold pool, and enjoy tranquility in our cozy relaxation area. In our sauna, each visit becomes a unique experience of rejuvenation and delight.</h5>
        <img src="@/assets/bath.png" alt="Bathhouse interior" class="w-full max-w-[995px] h-auto mt-8 rounded-2xl shadow-2xl">
        <button @click="modalState?.open()" class="border-2 md:border-4 border-white px-12 sm:px-[79px] py-4 sm:py-[22px] transition-all hover:text-black hover:bg-white duration-300 scale-100 translate-y-0 hover:scale-105 active:scale-95 cursor-pointer text-white text-2xl sm:text-4xl font-extrabold font-abhaya mt-9 sm:mt-11">
            Reserve
        </button>
    </section>
</template>

<script setup lang="js">
import { inject } from 'vue'

const modalState = inject('modalState')
</script>
