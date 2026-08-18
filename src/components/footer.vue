<template>
    <footer class="bg-black px-5 sm:px-8 lg:px-16 xl:px-[120px] pt-14 sm:pt-[90px] pb-28 md:pb-6 flex flex-col justify-end items-center">
        <div class="flex flex-col md:flex-row gap-10 md:gap-8 justify-between w-full max-w-[1200px]">
            <button class="flex flex-col items-start md:items-center space-x-2 bg-transparent">
                <img src="@/assets/logo.svg" alt="Spa Serenity Logo" class="w-14">
                <span class="text-white text-xl font-extrabold font-abhaya">Spa Serenity</span>
            </button>
            <nav class="flex flex-col gap-1">
                <a href="#start" class="text-white text-2xl sm:text-3xl font-normal font-abhaya transition hover:text-white/70">Home</a>
                <a href="#aboutSec" class="text-white text-2xl sm:text-3xl font-normal font-abhaya transition hover:text-white/70">About Us</a>
                <a href="#massageSec" class="text-white text-2xl sm:text-3xl font-normal font-abhaya transition hover:text-white/70">Services</a>
            </nav>
            <div class="flex flex-col text-white text-lg sm:text-xl font-semibold font-crimson">
                Contact us: <br>
                (Concept) <br>
                <a href="#"><img class="mt-1.5 w-[50px] h-[50px]" src="@/assets/WhatsApp.svg" alt=""></a>
            </div>
        </div>
        <div class="text-white/70 text-sm sm:text-base font-normal font-crimson mt-12 text-center">
            SpaSerenity 2024. All rights reserved
        </div>
    </footer>
</template>
