<template>
  <div class="min-h-screen bg-white font-merriweather selection:bg-button/30">
    <!-- Page Header / Hero -->
    <div class="relative pt-16">
      <div class="relative h-[60vh] flex items-center justify-center overflow-hidden">
        <img src="../../public/img/about2.png" class="absolute inset-0 w-full h-full object-cover transition-transform duration-[2s] hover:scale-110" alt="About Us Banner">
        <!-- Overlay -->
        <div class="absolute inset-0 bg-gradient-to-r from-slate-900/90 via-slate-900/70 to-transparent"></div>
        
        <div class="relative container mx-auto px-6 lg:px-12 z-10">
          <div class="max-w-3xl">
            <span class="inline-block px-4 py-1.5 mb-6 text-sm font-bold tracking-[0.2em] text-button uppercase bg-button/10 border border-button/20 rounded-full backdrop-blur-md">
              WHO WE ARE
            </span>
            <h1 class="text-4xl md:text-6xl lg:text-7xl font-black text-white mb-6 leading-tight italic tracking-tight">
              Kenali Kami <br><span class="text-button">Lebih Jauh</span>
            </h1>
            <div class="w-24 h-2 bg-button rounded-full"></div>
          </div>
        </div>
      </div>
    </div>

    <!-- Company Intro Section -->
    <div class="py-24 container mx-auto px-6 lg:px-12">
      <div class="flex flex-col lg:flex-row gap-16 items-center">
        <div class="lg:w-1/2 relative">
          <div class="absolute -top-10 -left-10 w-40 h-40 bg-button/5 rounded-full blur-3xl"></div>
          <div class="relative z-10 bg-slate-50 p-4 rounded-[2.5rem] shadow-inner border border-slate-100 group">
            <img src="../../public/img/about1.svg" class="w-full h-auto rounded-[2rem] transition-transform duration-500 group-hover:scale-95" alt="Company Illustration">
          </div>
        </div>
        
        <div class="lg:w-1/2">
          <h2 class="text-4xl font-black text-slate-800 mb-8 leading-tight tracking-tight italic">
            PT. ADITYA <span class="text-button">ARTA ABADI</span>
          </h2>
          <div class="space-y-6 text-slate-600 text-lg leading-relaxed font-medium">
            <p>
              PT Aditya Arta Abadi adalah perusahaan teknologi yang berfokus pada pengembangan solusi digital inovatif untuk membantu bisnis dan organisasi berkembang di era transformasi digital. 
            </p>
            <p>
              Dengan pengalaman bertahun-tahun dalam industri IT, kami menghadirkan layanan IT Support, Pengembangan Web, Aplikasi Mobile (Android & iOS), serta Konsultasi IT yang dirancang khusus untuk meningkatkan efisiensi dan produktivitas bisnis Anda.
            </p>
            <div class="pt-6 flex gap-4">
              <div class="p-6 bg-slate-50 rounded-2xl border border-slate-100 flex-1">
                <h4 class="font-black text-slate-800 text-2xl mb-1">Misi Kami</h4>
                <p class="text-sm text-slate-500">Memberdayakan bisnis melalui teknologi digital yang cerdas.</p>
              </div>
              <div class="p-6 bg-slate-50 rounded-2xl border border-slate-100 flex-1">
                <h4 class="font-black text-slate-800 text-2xl mb-1">Visi Kami</h4>
                <p class="text-sm text-slate-500">Menjadi mitra transformasi digital terdepan di Indonesia.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Services Section -->
    <div class="py-24 bg-slate-900 relative overflow-hidden">
      <div class="absolute top-0 left-0 w-full h-full opacity-10 pointer-events-none">
        <div class="absolute top-0 right-0 w-[500px] h-[500px] bg-button rounded-full blur-[120px]"></div>
      </div>
      
      <div class="container mx-auto px-6 lg:px-12 relative z-10">
        <div class="text-center mb-20">
          <h2 class="text-4xl md:text-5xl font-black text-white mb-4 italic tracking-tight">
            Layanan <span class="text-button">Unggulan</span> Kami
          </h2>
          <p class="text-slate-400 max-w-2xl mx-auto font-medium">Kami menyediakan ekosistem solusi digital yang komprehensif untuk mendukung setiap aspek kebutuhan teknologi perusahaan Anda.</p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <div v-for="(service, idx) in services" :key="idx" 
            class="group bg-slate-800/40 backdrop-blur-md p-8 rounded-[2rem] border border-slate-700/50 hover:border-button/50 transition-all duration-500 hover:-translate-y-2">
            <div class="flex flex-col lg:flex-row gap-8 items-start">
              <div class="w-32 h-32 flex-shrink-0 bg-slate-700/50 rounded-2xl p-4 flex items-center justify-center transition-all duration-500 group-hover:bg-button group-hover:scale-110">
                <img :src="service.icon" :alt="service.title" class="w-full h-full object-contain transition-transform duration-500 group-hover:scale-110">
              </div>
              <div class="flex-grow">
                <h3 class="text-2xl font-bold text-white mb-4 group-hover:text-button transition-colors">{{ service.title }}</h3>
                <p class="text-slate-400 leading-relaxed font-medium">{{ service.desc }}</p>
                
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const services = [
  {
    title: "Web Development",
    desc: "Kami membangun website profesional yang responsif, cepat, dan didesain secara khusus untuk meningkatkan kredibilitas brand Anda di dunia digital.",
    icon: "/img/web.svg"
  },
  {
    title: "Mobile App Development",
    desc: "Solusi aplikasi Android dan iOS yang inovatif, performa tinggi, dan fokus pada user experience (UX) terbaik untuk pengguna Anda.",
    icon: "/img/android.svg"
  },
  {
    title: "IT Consulting",
    desc: "Pendampingan strategis untuk perencanaan, implementasi, hingga optimasi infrastruktur IT agar sejalan dengan tujuan bisnis jangka panjang.",
    icon: "/img/itconsult.svg"
  },
  {
    title: "IT Support & Managed Services",
    desc: "Dukungan teknis menyeluruh untuk perangkat keras, lunak, hingga keamanan jaringan agar operasional bisnis Anda tetap lancar tanpa hambatan.",
    icon: "/img/dekstop.svg"
  }
];
</script>