<template>
  <header 
    :class="[
      'fixed top-0 left-0 w-full z-50 transition-all duration-500',
      isScrolled ? 'bg-white/95 backdrop-blur-md shadow-xl py-3' : 'bg-gradient-to-b from-black/60 to-transparent py-5'
    ]"
  >
    <div class="container mx-auto max-w-screen-xl flex items-center justify-between px-6 lg:px-12">
      <!-- Logo (Original Structure Preserved & Size Constrained) -->
      <div class="relative z-10">
        <a href="/" @click="scrollToTop" class="block">
          <div class="h-8 lg:h-10 w-48 lg:w-64 flex items-center">
            <img 
              :src="isScrolled ? '/img/logo3a.png' : '/img/logo3a-white.png'" 
              alt="3a Logo" 
              class="max-h-full max-w-full object-contain object-left transition-all duration-500 hover:scale-105"
            >
          </div>
        </a>
      </div>

      <!-- Desktop Navbar Menu -->
      <nav class="hidden lg:block">
        <ul class="flex items-center space-x-2">
          <li v-for="item in navItems" :key="item.path">
            <RouterLink
              :to="item.path"
              @click="scrollToTop"
              :class="[
                'relative px-5 py-2 text-[15px] font-bold tracking-wide transition-all duration-300 rounded-full group',
                route.path === item.path 
                  ? (isScrolled ? 'text-button' : 'text-button bg-white/10') 
                  : (isScrolled ? 'text-slate-700 hover:text-button' : 'text-white hover:text-button')
              ]"
            >
              {{ item.name }}
              <span 
                :class="[
                  'absolute bottom-1 left-1/2 -translate-x-1/2 w-0 h-1 bg-button rounded-full transition-all duration-300 group-hover:w-5',
                  route.path === item.path ? 'w-5' : ''
                ]"
              ></span>
            </RouterLink>
          </li>
          <li class="pl-6">
            <RouterLink 
              to="/contact-us"
              class="px-8 py-2.5 bg-button text-white text-xs font-black uppercase tracking-widest rounded-full shadow-lg shadow-button/30 hover:scale-105 hover:-translate-y-0.5 active:scale-95 transition-all duration-300"
            >
              Contact Us
            </RouterLink>
          </li>
        </ul>
      </nav>

      <!-- Hamburger Menu Button -->
      <button
        @click="isMenuOpen = !isMenuOpen"
        class="lg:hidden relative z-50 w-10 h-10 flex flex-col justify-center items-center focus:outline-none bg-button/10 rounded-xl"
      >
        <div class="w-5 h-4 flex flex-col justify-between">
          <span
            :class="[
              'w-full h-0.5 transition-all duration-300',
              isMenuOpen ? 'rotate-45 translate-y-[7px] bg-slate-800' : (isScrolled ? 'bg-slate-800' : 'bg-white')
            ]"
          ></span>
          <span
            :class="[
              'w-full h-0.5 transition-all duration-300',
              isMenuOpen ? 'opacity-0' : (isScrolled ? 'bg-slate-800' : 'bg-white')
            ]"
          ></span>
          <span
            :class="[
              'w-full h-0.5 transition-all duration-300',
              isMenuOpen ? '-rotate-45 -translate-y-[7px] bg-slate-800' : (isScrolled ? 'bg-slate-800' : 'bg-white')
            ]"
          ></span>
        </div>
      </button>

      <!-- Mobile Menu Overlay -->
      <Transition name="fade">
        <div v-if="isMenuOpen" class="fixed inset-0 bg-slate-900/80 backdrop-blur-sm lg:hidden z-40"></div>
      </Transition>

      <!-- Mobile Menu Side Panel -->
      <Transition name="slide">
        <nav
          v-if="isMenuOpen"
          class="fixed top-0 right-0 h-full w-[80%] max-w-sm bg-white shadow-2xl z-50 flex flex-col lg:hidden"
        >
          <div class="p-8 flex justify-between items-center border-b border-slate-50">
             <img src="/img/logo3a.png" alt="3a Logo" class="h-8 w-auto object-contain">
             <button @click="isMenuOpen = false" class="text-slate-400 hover:text-button p-2">
               <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                 <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
               </svg>
             </button>
          </div>
          
          <ul class="flex flex-col p-8 space-y-6">
            <li v-for="item in navItems" :key="item.path">
              <RouterLink
                :to="item.path"
                @click="closeMenu"
                :class="[
                  'block text-2xl font-bold transition-all duration-300',
                  route.path === item.path ? 'text-button translate-x-2' : 'text-slate-800 hover:text-button hover:translate-x-2'
                ]"
              >
                {{ item.name }}
              </RouterLink>
            </li>
          </ul>

          <div class="mt-auto p-8 border-t border-slate-50 bg-slate-50">
            <RouterLink 
              to="/contact-us"
              @click="closeMenu"
              class="w-full py-4 bg-button text-white font-bold rounded-2xl flex items-center justify-center gap-2 shadow-xl shadow-button/20"
            >
              Hubungi Kami <span class="text-xl">→</span>
            </RouterLink>
          </div>
        </nav>
      </Transition>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";
import { useRoute } from "vue-router";

const route = useRoute();
const isMenuOpen = ref(false);
const isScrolled = ref(false);

const navItems = [
  { name: 'Home', path: '/' },
  { name: 'About Us', path: '/about' },
  { name: 'Portfolio', path: '/portofolio' },
  
];

const handleScroll = () => {
  isScrolled.value = window.scrollY > 20;
};

const closeMenu = () => {
  isMenuOpen.value = false;
  scrollToTop();
};

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth',
  });
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.4s ease;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}

.slide-enter-active, .slide-leave-active {
  transition: transform 0.5s cubic-bezier(0.16, 1, 0.3, 1);
}
.slide-enter-from, .slide-leave-to {
  transform: translateX(100%);
}

.router-link-active span {
  width: 1.5rem;
}
</style>

