<template>
  <div class="min-h-screen bg-slate-50 font-merriweather selection:bg-button/30">
    <!-- Hero Section -->
    <div class="relative overflow-hidden">
      <section class="relative h-[80vh] lg:h-[90vh] flex items-center justify-center bg-center bg-no-repeat bg-cover transition-all duration-700"
        :style="{ backgroundImage: `url('/src/assets/img/bg-hero2.jpg')` }">
        <!-- Gradient Overlay -->
        <div class="absolute inset-0 bg-gradient-to-b from-slate-900/80 via-slate-900/60 to-slate-900/90"></div>
        
        <div class="relative px-6 mx-auto max-w-screen-xl text-center z-10">
          <span class="inline-block px-4 py-1.5 mb-6 text-sm font-semibold tracking-wider text-white uppercase bg-button/20 border border-button/30 rounded-full backdrop-blur-sm animate-fade-in">
            Digital Transformation Partner
          </span>
          <h1 class="mb-6 text-5xl font-extrabold tracking-tight leading-tight text-white md:text-6xl lg:text-7xl">
            Membangun <span class="text-transparent bg-clip-text bg-gradient-to-r from-button to-orange-400">Solusi Digital</span> <br>untuk Masa Depan
          </h1>
          <p class="mb-10 text-lg font-light text-gray-200 lg:text-xl max-w-3xl mx-auto leading-relaxed">
            Dari strategi hingga implementasi, kami membantu bisnis beradaptasi dan tumbuh pesat di era digital yang dinamis.
          </p>
          <div class="flex flex-col space-y-4 sm:flex-row sm:justify-center sm:space-y-0 sm:space-x-6">
            <a href="/about" class="group relative inline-flex items-center justify-center py-4 px-8 text-base font-bold text-white transition-all duration-300 bg-button rounded-xl hover:bg-button/90 hover:scale-105 shadow-lg shadow-button/25">
              Explore Our Story
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 ml-2 group-hover:translate-x-1 transition-transform" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6" />
              </svg>
            </a>
            <a href="/contact-us" class="inline-flex items-center justify-center py-4 px-8 text-base font-bold text-white transition-all duration-300 border-2 border-white/30 rounded-xl hover:bg-white/10 backdrop-blur-md hover:border-white">
              Get in Touch
            </a>  
          </div>
        </div>
      </section>

      <!-- Floating Feature Cards -->
      <div class="relative -mt-24 lg:-mt-32 px-6 max-w-screen-xl mx-auto z-20">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <!-- Card 1: Layanan -->
          <div class="group bg-white/80 backdrop-blur-xl p-8 rounded-3xl shadow-2xl shadow-slate-200/50 border border-white/50 hover:-translate-y-3 transition-all duration-500">
            <div class="w-14 h-14 mb-6 flex items-center justify-center rounded-2xl bg-button/10 text-button group-hover:bg-button group-hover:text-white transition-colors duration-300">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 13.255A23.931 23.931 0 0112 15c-3.183 0-6.22-.62-9-1.745M16 6V4a2 2 0 00-2-2h-4a2 2 0 00-2 2v2m4 6h.01M5 20h14a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
              </svg>
            </div>
            <h3 class="text-2xl font-bold text-slate-800 mb-4 tracking-tight uppercase">Layanan</h3>
            <div class="w-12 h-1 bg-button mb-6 group-hover:w-20 transition-all duration-500"></div>
            <p class="text-slate-600 leading-relaxed mb-8">
              Pembuatan website, pengembangan aplikasi Android, konsultasi IT, dan IT support yang dirancang untuk efisiensi bisnis Anda.
            </p>
            <RouterLink to="/about" class="inline-flex items-center font-bold text-button group-hover:gap-2 transition-all">
              Selengkapnya <span class="opacity-0 group-hover:opacity-100 transition-all">→</span>
            </RouterLink>
          </div>

          <!-- Card 2: Berpengalaman -->
          <div class="group bg-white/80 backdrop-blur-xl p-8 rounded-3xl shadow-2xl shadow-slate-200/50 border border-white/50 hover:-translate-y-3 transition-all duration-500">
            <div class="w-14 h-14 mb-6 flex items-center justify-center rounded-2xl bg-indigo-500/10 text-indigo-500 group-hover:bg-indigo-500 group-hover:text-white transition-colors duration-300">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
            </div>
            <h3 class="text-2xl font-bold text-slate-800 mb-4 tracking-tight uppercase">Berpengalaman</h3>
            <div class="w-12 h-1 bg-indigo-500 mb-6 group-hover:w-20 transition-all duration-500"></div>
            <p class="text-slate-600 leading-relaxed mb-8">
              Sejak 2009, kami telah membangun kepercayaan dengan berbagai perusahaan besar di seluruh Indonesia.
            </p>
            <RouterLink to="/portofolio" class="inline-flex items-center font-bold text-indigo-500 group-hover:gap-2 transition-all">
              Portfolio Kami <span class="opacity-0 group-hover:opacity-100 transition-all">→</span>
            </RouterLink>
          </div>

          <!-- Card 3: CTA -->
          <div class="relative overflow-hidden p-8 rounded-3xl shadow-2xl shadow-button/20 bg-button text-white flex flex-col justify-between group">
            <div class="absolute -top-10 -right-10 w-40 h-40 bg-white/10 rounded-full blur-3xl"></div>
            <div class="relative z-10">
              <h3 class="text-3xl font-black mb-6 leading-tight">Butuh Bantuan? Kami Siap Melayani Anda.</h3>
              <p class="text-white/80 mb-8 font-medium">Konsultasikan kebutuhan teknologi Anda bersama tim ahli kami secara gratis.</p>
            </div>
            <RouterLink to="/contact-us" class="relative z-10 w-full bg-white text-button py-4 rounded-xl font-bold text-center hover:bg-slate-100 transition-colors shadow-lg">
              Hubungi Kami Sekarang
            </RouterLink>
          </div>
        </div>
      </div>
    </div>

    <!-- Authorized Implementator Section -->
    <section class="py-24 bg-slate-900 relative overflow-hidden group mt-10">
      <div class="absolute top-0 right-0 w-96 h-96 bg-button/10 rounded-full blur-[120px] -mr-48 -mt-48 transition-all duration-700 group-hover:bg-button/20"></div>
      <div class="absolute bottom-0 left-0 w-96 h-96 bg-blue-500/10 rounded-full blur-[120px] -ml-48 -mb-48 transition-all duration-700 group-hover:bg-blue-500/20"></div>

      <div class="container mx-auto px-6 lg:px-12 relative z-10">
        <div class="max-w-5xl mx-auto bg-white/5 backdrop-blur-xl border border-white/10 rounded-[3rem] p-8 md:p-16 transition-all duration-500 hover:border-button/30 hover:shadow-2xl hover:shadow-button/10 group/card">
          <div class="flex flex-col lg:flex-row items-center gap-12">
            <!-- Logo Section -->
            <div class="lg:w-1/3 text-center">
              <div class="relative inline-block p-1 rounded-[2.5rem] bg-gradient-to-tr from-button to-orange-400 shadow-2xl shadow-button/20 transform transition-transform duration-700 group-hover/card:scale-110">
                <div class="bg-white p-8 rounded-[2.4rem]">
                  <img src="/img/automa/automa-logo.jpeg" alt="Automa Logo" class="w-32 md:w-40 mx-auto">
                </div>
              </div>
            </div>

            <!-- Content Section -->
            <div class="lg:w-2/3 text-center lg:text-left">
              <span class="inline-block px-4 py-1.5 mb-5 text-[10px] font-black tracking-[0.3em] text-button uppercase bg-button/10 border border-button/20 rounded-full">
                OFFICIAL PARTNERSHIP
              </span>
              <h2 class="text-2xl md:text-3xl font-black text-white mb-4 italic tracking-tight leading-tight">
                Authorized <span class="text-button text-shadow-glow">Implementator</span> Automa
              </h2>
              <p class="text-slate-400 text-sm md:text-base font-medium leading-relaxed mb-6">
                Kami bangga menjadi mitra resmi tersertifikasi untuk mengimplementasikan solusi teknologi canggih dari Automa. Memastikan bisnis Anda berjalan dengan standar efisiensi tertinggi.
              </p>
              
              <RouterLink to="/automa-detail" class="inline-flex items-center gap-3 py-3 px-8 bg-button text-white text-sm font-black rounded-xl shadow-2xl shadow-button/40 hover:bg-button/90 hover:-translate-y-1 active:scale-[0.98] transition-all group/btn">
                LIHAT DETAIL SERTIFIKASI
                <span class="text-lg transition-transform duration-300 group-hover/btn:translate-x-2">→</span>
              </RouterLink>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Team Section -->
    <div class="mt-32 py-24 bg-slate-900 overflow-hidden relative">
      <div class="absolute inset-0 bg-[radial-gradient(circle_at_30%_50%,#ff6e6c10,transparent_50%)]"></div>
      
      <div class="relative z-10 container mx-auto px-6">
        <div class="text-center mb-16">
          <span class="text-button font-bold tracking-[0.2em] uppercase text-sm mb-4 block">Our Excellence</span>
          <h2 class="text-4xl md:text-5xl font-black text-white mb-4 italic tracking-tight">Meet the Creative Minds</h2>
          <div class="w-24 h-1.5 bg-button mx-auto rounded-full"></div>
        </div>

        <swiper
          :effect="'coverflow'"
          :grabCursor="true"
          :centeredSlides="true"
          :slidesPerView="3"
          :spaceBetween="30"
          :coverflowEffect="{
            rotate: 20,
            stretch: 0,
            depth: 200,
            modifier: 1,
            slideShadows: false,
          }"
          :pagination="{ clickable: true }"
          :autoplay="{ delay: 3000, disableOnInteraction: false }"
          :modules="modules"
          class="teamSwiper !pb-20"
          :breakpoints="{
            320: { slidesPerView: 1.2, spaceBetween: 20 },
            768: { slidesPerView: 2, spaceBetween: 30 },
            1024: { slidesPerView: 3.5, spaceBetween: 40 }
          }"
        >
          <swiper-slide v-for="(member, index) in teamMembers" :key="index">
            <div class="relative group bg-slate-800 rounded-[2.5rem] p-4 border border-slate-700 transition-all duration-500 hover:border-button/50">
              <div class="relative aspect-[4/5] overflow-hidden rounded-[2rem]">
                <img class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110" :src="member.image" :alt="member.name">
                <div class="absolute inset-0 bg-gradient-to-t from-slate-900 via-transparent to-transparent opacity-60 group-hover:opacity-80 transition-opacity"></div>
                
                <!-- Social Placeholder -->
                <div class="absolute top-4 right-4 flex flex-col gap-2 translate-x-10 opacity-0 group-hover:translate-x-0 group-hover:opacity-100 transition-all duration-500">
                  <div class="w-10 h-10 bg-white/10 backdrop-blur-md border border-white/20 rounded-full flex items-center justify-center text-white hover:bg-button transition-colors">
                    <i class="fab fa-linkedin-in text-sm"></i>
                  </div>
                </div>
              </div>
              
              <div class="pt-6 pb-2 text-center">
                <h3 class="text-xl font-bold text-white mb-1 group-hover:text-button transition-colors">{{ member.name }}</h3>
                <p class="text-slate-400 text-sm font-medium uppercase tracking-widest">{{ member.position }}</p>
              </div>
            </div>
          </swiper-slide>
        </swiper>
      </div>
    </div>

    <!-- Why Choose Us -->
    <div class="py-32 bg-white relative overflow-hidden">
      <div class="absolute top-0 right-0 -translate-y-1/2 translate-x-1/4 w-[600px] h-[600px] bg-slate-50 rounded-full blur-3xl"></div>
      
      <div class="container mx-auto px-6 relative z-10">
        <div class="flex flex-col lg:flex-row items-center gap-16">
          <div class="lg:w-1/2">
            <h2 class="text-4xl md:text-5xl font-black text-slate-800 mb-8 leading-tight italic">
              Kenapa Partner Kami Selalu <span class="text-button">Kembali?</span>
            </h2>
            <p class="text-slate-600 text-lg mb-10 leading-relaxed max-w-xl">
              Kami tidak hanya menjual produk digital, kami membangun ekosistem yang berkelanjutan untuk pertumbuhan bisnis Anda di masa depan.
            </p>
            <div class="grid grid-cols-2 gap-6 mb-12">
              <div class="p-6 bg-slate-50 rounded-2xl border border-slate-100">
                <div class="text-3xl font-black text-slate-800 mb-2">15+</div>
                <div class="text-sm text-slate-500 uppercase tracking-widest font-bold">Years Experience</div>
              </div>
              <div class="p-6 bg-slate-50 rounded-2xl border border-slate-100">
                <div class="text-3xl font-black text-slate-800 mb-2">200+</div>
                <div class="text-sm text-slate-500 uppercase tracking-widest font-bold">Projects Done</div>
              </div>
            </div>
          </div>

          <div class="lg:w-1/2 grid gap-6">
            <div v-for="(reason, idx) in reasons" :key="idx" 
              class="flex items-start gap-6 bg-white p-6 rounded-2xl shadow-sm border border-slate-100 hover:shadow-xl hover:border-button/20 transition-all duration-300 group">
              <div class="flex-shrink-0 w-12 h-12 rounded-xl bg-slate-50 flex items-center justify-center text-button group-hover:bg-button group-hover:text-white transition-all duration-300 shadow-inner">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
              </div>
              <div>
                <h4 class="text-xl font-bold text-slate-800 mb-2">{{ reason.title }}</h4>
                <p class="text-slate-600 text-sm leading-relaxed">{{ reason.desc }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>

import axios from "axios";
import CardArticle from "@/components/CardArticle.vue";
import CardNewsEvent from "@/components/CardNewsEvent.vue";
import { Swiper, SwiperSlide } from 'swiper/vue';
import { EffectCoverflow, Pagination, Autoplay } from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/effect-coverflow';
import 'swiper/css/pagination';
import "swiper/css/autoplay";

// import Members from "@/components/Members.vue";
export default {
  components: {
    CardArticle,
    CardNewsEvent,
    Swiper,
    SwiperSlide,
    // Members,
  },
  data() {
    return {
      articles: [], // All articles fetched from API
      newsAndEvents: [], // All news and events fetched from API
      loading: true, // Loading state to show spinner while fetching data
      modules: [EffectCoverflow, Pagination, Autoplay],
      teamMembers: [
        { name: "Robi Ilham", position: "Project Manajer", image: "/img/members/robi.jpeg" },
        { name: "Susanto Hadiwijaya", position: "Team Leader", image: "/img/members/santoo.jpeg" },
        { name: "Ahmad Riyanto", position: "Team Leader", image: "/img/members/riann.jpeg" },
        { name: "Nina", position: "Finance", image: "/img/members/nina.jpeg" },
        { name: "Nurhasanah ", position: "Senior Programmer", image: "/img/members/nur.jpeg" },
        { name: "Aini Rahmawati Adla ", position: "Programmer", image: "/img/members/aini.jpeg" },
        { name: "Rafli", position: "Programmer", image: "/img/members/rafli.jpeg" },
        { name: "Muhammad Hapidz", position: "Programmer", image: "/img/members/abin.jpeg" },
        { name: "Dicky Dermawan", position: "IT Support", image: "/img/members/dicky.jpeg" },
        { name: "Septian Maolidin", position: "Operator", image: "/img/members/tian.jpeg" },
      ],
      reasons: [
        { title: "Berpengalaman & Profesional", desc: "Tim ahli kami siap memberikan solusi terbaik untuk setiap tantangan teknologi bisnis Anda." },
        { title: "Teknologi Terkini", desc: "Mengadopsi teknologi terbaru memastikan sistem Anda aman, efisien, dan scalable." },
        { title: "Kustomisasi Total", desc: "Kami membangun solusi yang benar-benar sesuai dengan alur kerja dan kebutuhan unik Anda." },
        { title: "Dukungan & Maintenance", desc: "Pendampingan pasca-rilis untuk memastikan operasional sistem tetap optimal setiap saat." },
      ]
    };
  },
  computed: {
    // Get only a limited number of articles to display
    limitedArticles() {
      return this.articles.slice(0, 3); // Limit to 3 articles
    },
    limitedNewsevents() {
      return this.newsAndEvents.slice(0, 3); // Limit to 3 news/events
    }
  },
  mounted() {
    // Fetch articles data from API using axios
    axios
      .get("https://apitiggerid.tri3a.com/api/Contents/BySegmentArticle")
      .then((response) => {
        this.articles = response.data; // Store all API data in state
      })
      .catch((error) => {
        console.error("Error fetching articles:", error);
      });

    // Fetch news and events data from API
    axios
      .get("https://apitiggerid.tri3a.com/api/Contents/BySegmentNewsAndEvent")
      .then((response) => {
        this.newsAndEvents = response.data; // Store all news/events data
      })
      .catch((error) => {
        console.error("Error fetching news and events:", error);
      })
      .finally(() => {
        this.loading = false; // Set loading to false after both data are fetched
      });
  },
  methods: {
    // Scroll to top of the page
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: 'smooth',
      });
    },
  },
};

</script>


<style scoped>
.teamSwiper :deep(.swiper-pagination-bullet) {
  background: #ff6e6c;
  opacity: 0.3;
}
.teamSwiper :deep(.swiper-pagination-bullet-active) {
  opacity: 1;
  width: 24px;
  border-radius: 4px;
  transition: all 0.3s;
}

@keyframes fade-in {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
.animate-fade-in {
  animation: fade-in 1s ease-out forwards;
}
</style>
