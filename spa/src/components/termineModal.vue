<script setup lang="js">
import { VueDatePicker } from '@vuepic/vue-datepicker';
import '@vuepic/vue-datepicker/dist/main.css';
import { computed } from 'vue';
import { inject } from 'vue'
import { ref } from 'vue';

const modalState = inject('modalState')



const time = ref({
    hours: new Date().getHours(),
    minutes: new Date().getMinutes()
})
const date = ref(null);

const tomorrowPlaceholder = computed(() => {
  const tomorrow = new Date()
  tomorrow.setDate(tomorrow.getDate() + 1) // Прибавляем 1 день к текущей дате
  
  // Форматируем в привычный вид DD.MM.YYYY (например, 14.08.2026)
  const day = String(tomorrow.getDate()).padStart(2, '0')
  const month = String(tomorrow.getMonth() + 1).padStart(2, '0') // Месяцы в JS идут с 0
  const year = tomorrow.getFullYear()
  
  return `${month}.${day}.${year}`
})
</script>

<style>
input{
    color: #000;
}
</style>

<style>
.custom-datepicker {
  --dp-text-color: rgba(255, 255, 255, 0.6) !important;
  
  --dp-placeholder-color: rgba(255, 255, 255, 0.6) !important;
  
  --dp-background-color: #181215 !important;
  
  --dp-border-color: rgba(142, 129, 122, 0.13) !important;
}




</style>


<template>
    <Transition name="fade-bounce">
    <div class="fixed inset-0 w-full h-full bg-black/60 z-50 overflow-y-auto px-4 py-8"  v-if="modalState.isOpen">
        <div class="modal-content bg-[#0E090C] p-5 sm:p-9 relative w-full max-w-[560px] mx-auto my-auto top-1/2 -translate-y-1/2 rounded-lg border border-white/10 shadow-2xl">
            <p class="text-white text-3xl font-normal font-abhaya">Book Appointment</p>
            <p class="text-white/70 text-base font-normal font-crimson leading-6 mt-2">Secure your journey of relaxation and beauty. Choose your preferred time and share any special requests.</p>
            <form action="">
                <div class="flex flex-col sm:flex-row gap-4 sm:justify-between text-stone-500 text-sm font-normal font-abhaya mb-4 mt-5 uppercase tracking-wide">
                    <div class="w-full sm:w-[208px] font-crimson relative overflow-visible z-50">
                        <label for="">
                            DATE
                            <VueDatePicker class="custom-datepicker" v-model="date" dark :time-config="{ enableTimePicker: false }" teleport="body" :placeholder="tomorrowPlaceholder" :min-date="new Date()" auto-apply/>
                        </label>
                    </div>
                    <div class="w-full sm:w-[208px]">
                        <label for="">
                            TIME
                            <VueDatePicker class="custom-datepicker" dark v-model="time" time-picker />
                        </label>
                    </div>
                </div>
                <label for="instructions" class="flex flex-col text-stone-500 text-sm font-normal font-crimson uppercase tracking-wide">
                    Special Instructions
                    <textarea name="instructions" class="mt-1.5 bg-[#181215] rounded-sm p-4 min-h-28 resize-y text-white normal-case" placeholder="Any preferences or allergies our therapists should be aware of..."   id="instructions"></textarea>
                </label>
                <div class="flex flex-col-reverse sm:flex-row sm:justify-end gap-3 mt-7">
                    <button class="border border-white rounded-[5px] text-white text-base font-bold font-crimson px-6 py-3 cursor-pointer transition hover:bg-white hover:text-black" @click.prevent="modalState.close()">Cancel</button>
                    <button class="text-white bg-stone-500 py-3 px-6 text-base font-normal font-crimson cursor-pointer rounded-[5px] transition hover:bg-stone-400">Confirm Appointment</button>
                </div>
            </form>
        
        </div>
        
    </div>
    </Transition>
</template>

<style>
/* ==========================================================================
   МАГИЯ АНИМАЦИИ МОДАЛКИ (Vue 3 Transition)
   ========================================================================== */

/* 1. Фаза появления и исчезновения (задает время и функцию плавности) */
.fade-bounce-enter-active,
.fade-bounce-leave-active {
  transition: all 0.4s cubic-bezier(0.34, 1.56, 0.64, 1); /* Классный пружинящий эффект (bounce) */
}

/* Стилизация подложки внутри активной фазы */
.fade-bounce-enter-active opacity-60,
.fade-bounce-leave-active opacity-60 {
  transition: opacity 0.3s ease;
}

/* 2. Стартовая точка при появлении И конечная точка при закрытии */
.fade-bounce-enter-from,
.fade-bounce-leave-to {
  opacity: 0; /* Модалка полностью прозрачная */
}

/* Эффект для самого белого окна внутри модалки в момент старта/финиша */
.fade-bounce-enter-from .modal-content {
  opacity: 0;
  transform: scale(0.9) translateY(20px); /* Окно уменьшено на 10% и смещено вниз */
}

.fade-bounce-leave-to .modal-content {
  opacity: 0;
  transform: scale(0.95) translateY(10px); /* При закрытии мягко уходит вниз */
}
</style>
