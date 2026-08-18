<template>
    <section class="px-5 sm:px-8 lg:px-16 py-16 sm:py-20 relative flex flex-col items-center" id="reviews">
        <h6 class="text-white text-3xl sm:text-4xl font-extrabold font-abhaya mb-8 text-center">Last Reviews</h6>
        <div class="max-w-[996px] flex flex-col sm:flex-row gap-5 bg-black/75 backdrop-blur-sm p-5 sm:p-7 rounded-xl border border-white/10 shadow-2xl">
            <img src="@/assets/User.svg" alt="Natali avatar" class="w-16 h-16 sm:w-24 sm:h-24 shrink-0">
            <div class="text-white">
                <p class="text-white text-3xl sm:text-4xl font-extrabold font-abhaya">Natali</p>
                <p class="text-white/90 text-lg sm:text-xl font-normal font-crimson leading-relaxed mt-2">Unforgettable massage experience! I tried the Massage with organic ingredients at SpaSerenity, and it was pure bliss! The therapist was highly professional, and the natural oils left my skin feeling soft and refreshed. The whole experience was incredibly relaxing, and I felt completely rejuvenated afterward. Highly recommend for anyone looking to unwind!</p>
            </div>
        </div>
        <div class="max-w-[996px] flex flex-col sm:flex-row gap-5 bg-black/75 backdrop-blur-sm p-5 sm:p-7 rounded-xl border border-white/10 shadow-2xl mt-8 sm:mt-14">
            <img src="@/assets/User.svg" alt="Ann avatar" class="w-16 h-16 sm:w-24 sm:h-24 shrink-0">
            <div class="text-white">
                <p class="text-white text-3xl sm:text-4xl font-extrabold font-abhaya">Ann</p>
                <p class="text-white/90 text-lg sm:text-xl font-normal font-crimson leading-relaxed mt-2">The perfect spa escape! SpaSerenity offers an amazing selection of treatments, but my favorites were the Hot rain shower and Bathhouse experience. The warmth, steam, and soothing atmosphere helped melt away all stress and tension. It felt like a true wellness retreat! I can't wait to come back and try more services.</p>
            </div>
        </div>
        <button @click="modalState?.open()" class="transition-all hover:text-black hover:bg-white duration-300 scale-100 translate-y-0 hover:scale-105 active:scale-95 cursor-pointer border-2 md:border-4 border-white text-white text-2xl sm:text-4xl font-extrabold font-abhaya py-3 sm:py-4 mt-12 sm:mt-16 px-10 sm:px-[74px]">leave feedback</button>
    </section>
</template>

<script setup lang="js">
import { inject } from 'vue'

const modalState = inject('modalState')

</script>
