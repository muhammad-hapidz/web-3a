<template>
  <div class="min-h-screen bg-white font-merriweather selection:bg-button/30">
    <!-- Page Header / Hero -->
    <div class="relative pt-16">
      <div class="relative h-[40vh] flex items-center justify-center overflow-hidden">
        <img src="../../public/img/about2.png" class="absolute inset-0 w-full h-full object-cover transition-transform duration-[2s] hover:scale-110" alt="Contact Us Banner">
        <div class="absolute inset-0 bg-slate-900/80 backdrop-blur-[2px]"></div>
        
        <div class="relative container mx-auto px-6 lg:px-12 z-10 text-center">
          <span class="inline-block px-4 py-1.5 mb-6 text-sm font-black tracking-[0.3em] text-button uppercase bg-button/10 border border-button/20 rounded-full">
            GET IN TOUCH
          </span>
          <h1 class="text-4xl md:text-6xl font-black text-white italic tracking-tight">
            Hubungi <span class="text-button">Kami</span>
          </h1>
        </div>
      </div>
    </div>

    <!-- Contact Content Section -->
    <div class="py-24 container mx-auto px-6 lg:px-12">
      <div class="max-w-6xl mx-auto">
        <div class="text-center mb-16">
          <h2 class="text-3xl md:text-4xl font-black text-slate-800 mb-4 italic">Informasi Kontak</h2>
          <p class="text-slate-500 font-medium leading-relaxed max-w-2xl mx-auto">
            Kami siap membantu Anda! Jangan ragu untuk menghubungi kami melalui saluran di bawah ini jika memiliki pertanyaan atau ingin berdiskusi lebih lanjut tentang layanan kami.
          </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-20">
          <div class="group bg-white p-8 rounded-[2rem] border border-slate-100 shadow-sm hover:shadow-2xl hover:border-button/20 transition-all duration-500 text-center">
            <div class="w-20 h-20 bg-slate-50 rounded-3xl flex items-center justify-center text-button group-hover:bg-button group-hover:text-white transition-all duration-500 mx-auto mb-6 shadow-inner">
              <svg class="w-8 h-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/>
              </svg>
            </div>
            <h4 class="text-xs font-black text-slate-400 uppercase tracking-widest mb-3">Our Office</h4>
            <p class="text-slate-800 font-bold leading-relaxed">
              Ruko Victorian Bintaro-Pd. Karya Blok CC06, Kec. Pd. Aren, Kota Tangerang Selatan, Banten 15225.
            </p>
          </div>

          <div class="group bg-white p-8 rounded-[2rem] border border-slate-100 shadow-sm hover:shadow-2xl hover:border-button/20 transition-all duration-500 text-center">
            <div class="w-20 h-20 bg-slate-50 rounded-3xl flex items-center justify-center text-button group-hover:bg-button group-hover:text-white transition-all duration-500 mx-auto mb-6 shadow-inner">
              <svg class="w-8 h-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
              </svg>
            </div>
            <h4 class="text-xs font-black text-slate-400 uppercase tracking-widest mb-3">Email Us</h4>
            <a href="mailto:info@tri3a.com" class="text-slate-800 font-black text-xl md:text-2xl hover:text-button transition-colors">info@tri3a.com</a>
          </div>

          <div class="group bg-white p-8 rounded-[2rem] border border-slate-100 shadow-sm hover:shadow-2xl hover:border-button/20 transition-all duration-500 text-center">
            <div class="w-20 h-20 bg-slate-50 rounded-3xl flex items-center justify-center text-button group-hover:bg-button group-hover:text-white transition-all duration-500 mx-auto mb-6 shadow-inner">
              <svg class="w-8 h-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z" />
              </svg>
            </div>
            <h4 class="text-xs font-black text-slate-400 uppercase tracking-widest mb-3">Call Support</h4>
            <p class="text-slate-800 font-black text-xl md:text-2xl">+62 21 1234 5678</p>
          </div>
        </div>

        <!-- Social Illustration Section -->
        <div class="relative max-w-4xl mx-auto p-1 bg-button rounded-[3rem] shadow-2xl shadow-button/20 mb-20">
          <div class="bg-white p-12 rounded-[2.9rem] flex flex-col md:flex-row items-center gap-12">
            <div class="md:w-1/3">
              <img src="../../public/img/contact.svg" class="w-full drop-shadow-2xl" alt="Contact Illustration">
            </div>
            <div class="md:w-2/3 text-center md:text-left">
              <h4 class="font-black text-slate-800 text-3xl mb-4 italic">Let's Connect!</h4>
              <p class="text-slate-500 font-medium mb-8">Ikuti perjalanan kami dan temukan solusi digital terbaru melalui media sosial kami.</p>
              <div class="flex justify-center md:justify-start gap-6">
                <a href="https://www.instagram.com/zahraideaprima/" class="w-14 h-14 rounded-2xl bg-slate-50 flex items-center justify-center text-slate-400 hover:bg-button hover:text-white hover:-translate-y-2 transition-all duration-500 shadow-sm">
                  <i class="fab fa-instagram text-2xl"></i>
                </a>
                <a href="#" class="w-14 h-14 rounded-2xl bg-slate-50 flex items-center justify-center text-slate-400 hover:bg-button hover:text-white hover:-translate-y-2 transition-all duration-500 shadow-sm">
                  <i class="fab fa-linkedin-in text-2xl"></i>
                </a>
                <a href="https://wa.me/6285773256182" target="_blank" class="w-14 h-14 rounded-2xl bg-slate-50 flex items-center justify-center text-slate-400 hover:bg-[#25D366] hover:text-white hover:-translate-y-2 transition-all duration-500 shadow-sm">
                  <i class="fab fa-whatsapp text-2xl"></i>
                </a>
              </div>
            </div>
          </div>
        </div>

        <!-- Map Section -->
        <div class="h-[500px] w-full rounded-[3rem] overflow-hidden shadow-2xl border-4 border-white">
               <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3965.9527997202954!2d106.73664007543158!3d-6.269937993718762!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e69f148976f2bad%3A0x301db6590390b8c!2sRuko%20Victorian%20Bintaro!5e0!3m2!1sen!2sid!4v1778659048133!5m2!1sen!2sid" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
</style>