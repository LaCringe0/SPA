<template>
<section class="bg-[url(@/assets/main.png)] w-full bg-cover px-5 sm:px-8 lg:px-16 xl:px-[120px] py-16 sm:py-20" id="aboutSec">
    <div class="flex flex-col xl:grid xl:grid-cols-[minmax(0,691px)_1fr] w-full gap-10 xl:gap-0 max-w-[1440px] mx-auto relative">
        
        <div class="w-full xl:max-w-[691px] mt-6 xl:mt-[10.84%] flex flex-col items-start text-left z-10">
            <h2 class="text-white text-3xl md:text-4xl font-bold font-abhaya mb-5">
                Spa Serenity
            </h2>
            
            <h4 class="text-white text-base md:text-xl font-normal font-crimson text-pretty leading-relaxed mb-6">
                is where the art of caring for you comes to life. Our spa is designed to surround you with an atmosphere of tranquility and beauty. We offer not only high-quality body care procedures but also a unique experience filled with attention to detail. Our therapists are true professionals ready to create individual solutions for your relaxation and rejuvenation. Trust Spa Serenity and immerse yourself in a world of harmony and beauty, where every moment is dedicated to your well-being.
            </h4>
            
            <button class="border-2 md:border-4 border-white text-white text-2xl md:text-4xl font-extrabold font-abhaya px-10 sm:px-[71px] py-4 sm:py-[22px] transition-all hover:text-black hover:bg-white duration-300 scale-100 translate-y-0 hover:scale-105 active:scale-95 cursor-pointer">
                Contacts
            </button>
        </div>
        <div class="w-full relative mt-10 xl:mt-0 flex flex-col sm:flex-row xl:block items-center gap-6 justify-center">
            <img 
                src="@/assets/2.png" 
                alt="Spa 2" 
                class="w-full max-w-[387px] aspect-[387/533] object-cover rounded-2xl shadow-lg z-20 xl:mt-[400px] xl:-ml-[220px] block"
            >
            <img 
                src="@/assets/1.png" 
                alt="Spa 1" 
                class="xl:absolute xl:top-[0px] xl:right-0 w-full max-w-[387px] aspect-[387/533] object-cover rounded-2xl shadow-xl z-10"
            >
            
        </div>

    </div>
</section>

</template>
