<template>
  <div class="min-h-screen bg-slate-50 font-merriweather selection:bg-button/30">
    <!-- Hero Section -->
    <div class="relative pt-16">
      <div class="relative h-[70vh] lg:h-[85vh] flex items-center justify-center overflow-hidden">
        <img src="../assets/img/bg-port.jpg" class="absolute inset-0 w-full h-full object-cover transition-transform duration-[3s] hover:scale-110" alt="Portfolio Banner">
        <div class="absolute inset-0 bg-gradient-to-b from-slate-900/90 via-slate-900/70 to-slate-900/95"></div>
        
        <div class="relative container mx-auto px-6 lg:px-12 z-10 text-center">
          <span class="inline-block px-4 py-1.5 mb-6 text-sm font-bold tracking-[0.3em] text-white uppercase bg-button/20 border border-button/30 rounded-full backdrop-blur-md">
            OUR WORKS
          </span>
          <h1 class="text-5xl md:text-7xl lg:text-8xl font-black text-white mb-8 italic tracking-tight leading-none">
            Hasil Dari <br><span class="text-transparent bg-clip-text bg-gradient-to-r from-button to-orange-400">Pekerjaan Kami</span>
          </h1>
          <p class="text-gray-300 text-lg md:text-xl max-w-2xl mx-auto leading-relaxed font-light">
            Membangun masa depan digital melalui kolaborasi, inovasi, dan eksekusi yang presisi untuk setiap mitra kami.
          </p>
        </div>
      </div>
    </div>

    <!-- Intro Section -->
    <div class="py-24 container mx-auto px-6 lg:px-12">
      <div class="flex flex-col lg:flex-row gap-16 items-center">
        <div class="lg:w-1/2">
          <span class="text-button font-black tracking-widest text-sm uppercase mb-4 block">Trusted Expertise</span>
          <h2 class="text-4xl md:text-5xl font-black text-slate-800 mb-8 italic leading-tight">
            PT. ADITYA <span class="text-button">ARTA ABADI</span>
          </h2>
          <p class="text-slate-600 text-lg leading-relaxed mb-8 font-medium">
            Kami telah mengerjakan berbagai proyek strategis, mulai dari solusi korporat hingga instansi pemerintahan. Setiap proyek adalah kesempatan bagi kami untuk memberikan efisiensi, inovasi, dan nilai tambah yang nyata bagi bisnis klien kami.
          </p>
          <div class="flex flex-wrap gap-4">
            <div class="px-6 py-3 bg-white rounded-2xl shadow-sm border border-slate-100 font-bold text-slate-700 flex items-center gap-2">
              <span class="w-2 h-2 bg-button rounded-full"></span> Web Systems
            </div>
            <div class="px-6 py-3 bg-white rounded-2xl shadow-sm border border-slate-100 font-bold text-slate-700 flex items-center gap-2">
              <span class="w-2 h-2 bg-button rounded-full"></span> Mobile Apps
            </div>
            <div class="px-6 py-3 bg-white rounded-2xl shadow-sm border border-slate-100 font-bold text-slate-700 flex items-center gap-2">
              <span class="w-2 h-2 bg-button rounded-full"></span> Cloud Support
            </div>
          </div>
        </div>
        
        <div class="lg:w-1/2 grid grid-cols-2 gap-4">
          <div class="rounded-[2rem] overflow-hidden shadow-2xl h-80 relative group">
            <img src="/img/portofolio1.jpg" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110" alt="Portfolio 1">
            <div class="absolute inset-0 bg-slate-900/20 group-hover:bg-slate-900/40 transition-colors"></div>
          </div>
          <div class="rounded-[2rem] overflow-hidden shadow-2xl h-80 mt-12 relative group">
            <img src="/img/portofolio2.jpg" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110" alt="Portfolio 2">
            <div class="absolute inset-0 bg-slate-900/20 group-hover:bg-slate-900/40 transition-colors"></div>
          </div>
        </div>
      </div>
    </div>

    <!-- Clients Section -->
    <div class="py-24 bg-white">
      <div class="container mx-auto px-6 lg:px-12">
        <div class="text-center mb-16">
          <h3 class="text-2xl font-black text-slate-800 italic">Siapa saja yang sudah bekerja sama dengan kami?</h3>
          <div class="w-20 h-1.5 bg-button mx-auto mt-4 rounded-full"></div>
        </div>
        
        <div class="flex flex-wrap justify-center gap-8 lg:gap-16 opacity-60 hover:opacity-100 transition-opacity duration-500">
          <img 
            v-for="(image, index) in images" 
            :key="index" 
            :src="image" 
            alt="Client Logo"
            class="h-12 md:h-16 w-auto object-contain grayscale hover:grayscale-0 transition-all duration-300"
          />
        </div>
      </div>
    </div>

    <!-- Portfolio Grid -->
    <div class="py-32 bg-slate-900 relative">
      <div class="absolute top-0 left-0 w-full h-full bg-[radial-gradient(circle_at_20%_20%,#ff6e6c05,transparent_50%)]"></div>
      
      <div class="container mx-auto px-6 lg:px-12 relative z-10">
        <div class="flex justify-between items-end mb-20">
          <div>
            <span class="text-button font-black tracking-widest text-sm uppercase mb-4 block">Case Studies</span>
            <h2 class="text-4xl md:text-5xl font-black text-white italic tracking-tight">Our <span class="text-button">Masterpieces</span></h2>
          </div>
          <div v-if="!portfolioStore.loading" class="hidden md:block text-slate-400 font-bold">
            Showing {{ portfolioStore.portfolios.length }} Projects
          </div>
        </div>

        <!-- Loading Indicator -->
        <div v-if="portfolioStore.loading" class="flex justify-center items-center py-24">
          <div class="w-16 h-16 border-4 border-button/30 border-t-button rounded-full animate-spin"></div>
        </div>

        <!-- Portofolio Grid -->
        <div v-else class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
          <div
            v-for="portfolio in portfolioStore.portfolios"
            :key="portfolio.id"
            class="group bg-slate-800/50 backdrop-blur-md rounded-[2.5rem] overflow-hidden border border-slate-700/50 hover:border-button/50 transition-all duration-500"
          >
            <div class="relative h-72 overflow-hidden">
              <img class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110" :src="portfolio.image" alt="Portfolio Image">
              <div class="absolute top-6 left-6 px-4 py-1.5 bg-button text-white text-xs font-black uppercase tracking-widest rounded-full shadow-lg">
                {{ portfolio.category.categoryName }}
              </div>
              <div class="absolute inset-0 bg-gradient-to-t from-slate-900 via-transparent to-transparent opacity-60"></div>
            </div>

            <div class="p-8">
              <h5 class="text-2xl font-bold text-white mb-4 group-hover:text-button transition-colors">
                {{ portfolio.title }}
              </h5>
              <div class="text-slate-400 text-sm leading-relaxed mb-6 font-medium line-clamp-3" v-html="portfolio.description"></div>
              <div class="flex items-center text-button font-bold text-xs uppercase tracking-widest group-hover:gap-2 transition-all">
                View Project Details <span class="opacity-0 group-hover:opacity-100 transition-all">→</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Testimonials -->
    <div class="py-32 bg-white overflow-hidden relative">
      <div class="absolute -bottom-24 -right-24 w-96 h-96 bg-button/5 rounded-full blur-3xl"></div>
      
      <div class="container mx-auto px-6 lg:px-12 relative z-10">
        <div class="text-center mb-20">
          <span class="text-button font-black tracking-widest text-sm uppercase mb-4 block">Feedback</span>
          <h2 class="text-4xl md:text-5xl font-black text-slate-800 italic tracking-tight">What They Say <span class="text-button">About Us</span></h2>
        </div>

        <div v-if="testimoniStore.loading" class="flex justify-center items-center py-20">
          <div class="w-12 h-12 border-4 border-slate-100 border-t-button rounded-full animate-spin"></div>
        </div>

        <div v-else class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
          <div
            v-for="testimoni in testimoniStore.testimonis"
            :key="testimoni.id"
            class="bg-slate-50 p-8 rounded-[2rem] border border-slate-100 hover:shadow-2xl hover:border-button/20 transition-all duration-500 group"
          >
            <div class="flex items-center gap-4 mb-6">
              <div class="w-16 h-16 rounded-2xl overflow-hidden shadow-lg border-2 border-white">
                <img class="w-full h-full object-cover" :src="testimoni.image || '/img/project-review.jpg'" alt="Client Avatar">
              </div>
              <div>
                <h5 class="font-bold text-slate-800 leading-tight">{{ testimoni.title }}</h5>
                <span class="text-button text-xs font-black uppercase tracking-wider">{{ testimoni.category.categoryName }}</span>
              </div>
            </div>
            <div class="relative">
              <svg class="absolute -top-4 -left-4 w-12 h-12 text-button/10" fill="currentColor" viewBox="0 0 32 32"><path d="M10 8v8H6v6h6V8h-2zm12 0v8h-4v6h6V8h-2z"/></svg>
              <div class="text-slate-600 leading-relaxed font-medium text-sm line-clamp-4 italic" v-html="testimoni.description"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { onMounted } from "vue";
import { usePortfolioStore } from "@/stores/usePortofolioStore";
import { useTestimoniStore } from "@/stores/useTestimoniStore";

const portfolioStore = usePortfolioStore();
const testimoniStore = useTestimoniStore();
const images = Object.entries(import.meta.glob("../../public/img/clients/*.png", { eager: true }))
  .map(([path, mod]) => ({
    path,
    src: mod.default || mod
  }))
  .sort((a, b) => a.path.localeCompare(b.path))
  .map(i => i.src);

onMounted(() => {
  portfolioStore.fetchPortfolios();
  testimoniStore.fetchTestimonis();
});
</script>

<style scoped>
.line-clamp-3 {
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  overflow: hidden;
}
.line-clamp-4 {
  display: -webkit-box;
  -webkit-line-clamp: 4;
  -webkit-box-orient: vertical;
  overflow: hidden;
}
</style>