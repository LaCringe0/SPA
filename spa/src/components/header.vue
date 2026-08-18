<template>
    <header class="bg-black/65 backdrop-blur-md py-2.5 px-4 sm:px-8 lg:px-16 xl:px-24 flex flex-row justify-between items-center fixed z-40 top-0 w-full">
        <a href="#start" class="flex flex-col items-center space-x-2 bg-transparent cursor-pointer">
            <img src="@/assets/logo.svg" alt="Spa Serenity Logo" class="w-10 sm:w-auto">
            <span class="text-white text-base sm:text-xl font-extrabold font-abhaya leading-none">Spa Serenity</span>
        </a>
        <nav class="hidden md:flex gap-8 lg:gap-16 xl:gap-28">
            <a href="#aboutSec" class="text-white relative inline-block text-xl lg:text-2xl font-normal font-abhaya group tracking-wide">About Us
                <span class="absolute left-0 bottom-[-6px] w-0 h-[2px] bg-white transition-all duration-300 ease-out group-hover:w-full"></span>
            </a>
            <a href="#massageSec" class="text-white relative inline-block text-xl lg:text-2xl font-normal font-abhaya group tracking-wide">Services
                <span class="absolute left-0 bottom-[-6px] w-0 h-[2px] bg-white transition-all duration-300 ease-out group-hover:w-full"></span>
            </a>
            <a href="#reviews" class="text-white relative inline-block text-xl lg:text-2xl font-normal font-abhaya group tracking-wide">Reviews
                <span class="absolute left-0 bottom-[-6px] w-0 h-[2px] bg-white transition-all duration-300 ease-out group-hover:w-full"></span>
            </a>

        </nav>
        <button class="cursor-pointer rounded-full border border-white/20 bg-white/10 p-2 transition hover:bg-white/20" @click="modalState?.open()">
            <img src="@/assets/Contacts.svg" alt="Open contacts" class="w-7 sm:w-9">
        </button>
    </header>
    <nav class="fixed bottom-4 left-1/2 z-40 flex w-[calc(100%-32px)] max-w-[420px] -translate-x-1/2 items-center justify-between rounded-full border border-white/15 bg-black/75 px-3 py-2 shadow-2xl backdrop-blur-md md:hidden">
        <a href="#start" class="flex min-w-0 flex-1 flex-col items-center gap-1 rounded-full px-2 py-1.5 text-white/80 transition hover:bg-white/10 hover:text-white">
            <svg class="h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
                <path d="m3 10.5 9-7 9 7" />
                <path d="M5 9.5V21h14V9.5" />
                <path d="M9 21v-6h6v6" />
            </svg>
            <span class="text-xs font-semibold font-crimson leading-none">Home</span>
        </a>
        <a href="#massageSec" class="flex min-w-0 flex-1 flex-col items-center gap-1 rounded-full px-2 py-1.5 text-white/80 transition hover:bg-white/10 hover:text-white">
            <svg class="h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
                <path d="M4 19h16" />
                <path d="M5 19V9a4 4 0 0 1 4-4h6a4 4 0 0 1 4 4v10" />
                <path d="M8 12h8" />
                <path d="M8 15h8" />
            </svg>
            <span class="text-xs font-semibold font-crimson leading-none">Services</span>
        </a>
        <button class="-mt-8 flex h-16 w-16 shrink-0 flex-col items-center justify-center rounded-full border border-white/30 bg-white text-black shadow-xl transition hover:scale-105 active:scale-95" @click="modalState?.open()">
            <svg class="h-6 w-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.9" stroke-linecap="round" stroke-linejoin="round">
                <path d="M8 2v4" />
                <path d="M16 2v4" />
                <rect width="18" height="18" x="3" y="4" rx="2" />
                <path d="M3 10h18" />
                <path d="M9 15h.01" />
                <path d="M15 15h.01" />
            </svg>
            <span class="text-xs font-bold font-crimson leading-none">Book</span>
        </button>
        <a href="#reviews" class="flex min-w-0 flex-1 flex-col items-center gap-1 rounded-full px-2 py-1.5 text-white/80 transition hover:bg-white/10 hover:text-white">
            <svg class="h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
                <path d="M12 17.5 6.8 20l1-5.8-4.2-4.1 5.8-.8L12 4l2.6 5.3 5.8.8-4.2 4.1 1 5.8Z" />
            </svg>
            <span class="text-xs font-semibold font-crimson leading-none">Reviews</span>
        </a>
        <button class="flex min-w-0 flex-1 flex-col items-center gap-1 rounded-full px-2 py-1.5 text-white/80 transition hover:bg-white/10 hover:text-white" @click="modalState?.open()">
            <svg class="h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
                <path d="M21 15a4 4 0 0 1-4 4H8l-5 3V7a4 4 0 0 1 4-4h10a4 4 0 0 1 4 4Z" />
                <path d="M8 9h8" />
                <path d="M8 13h5" />
            </svg>
            <span class="text-xs font-semibold font-crimson leading-none">Contact</span>
        </button>
    </nav>
</template>

<script setup lang="js">
import { inject } from 'vue'

const modalState = inject('modalState')

</script>



