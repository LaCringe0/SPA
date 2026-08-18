<script setup lang="js">
import headerComponent from './components/header.vue'
import homeView from './views/homeView.vue';
import aboutUs from './views/aboutUs.vue';
import './style.css'
import Massage from './views/massage.vue';
import Shugaring from './views/shugaring.vue';
import Shower from './views/shower.vue';
import Bath from './views/bath.vue';
import Revievs from './views/revievs.vue';
import FooterComponent from './components/footer.vue';
import TermineModal from './components/termineModal.vue';
import { ref, provide, reactive } from 'vue'


const isOpen = ref(false)

const modalState = reactive({
  isOpen: false,
  open() { this.isOpen = true },
  close() { this.isOpen = false }
})

provide('modalState', modalState)
</script>


<template>
  <section>
    <TermineModal />
    <headerComponent />
    <homeView />
    <aboutUs />
    <div class="bg-[linear-gradient(rgba(0,0,0,0.5),rgba(0,0,0,0.5)),url(@/assets/mainphotopeach.png)] bg-cover">
      <Massage />
      <Shugaring />
      <Shower />
      <Bath />
      <Revievs />
    </div>
    <FooterComponent />
    
  </section>
</template>

<style scoped>

</style>
