<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CNC Fitness BSB - Pusat Kebugaran Premium di Balikpapan</title>
    
    <script src="https://cdn.tailwindcss.com"></script>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;900&display=swap" rel="stylesheet">
    
    <link rel="icon" href="https://placehold.co/32x32/1a1a1a/FFFFFF?text=CNC" type="image/png" onerror="this.onerror=null;this.src='https://placehold.co/32x32';">

    <style>
        /* Default Font & New Fixed Background */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0A0A0A; /* Fallback color */
            color: #e5e7eb;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
            
            background-image: linear-gradient(rgba(10, 10, 10, 0.92), rgba(10, 10, 10, 0.92)), url('https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3');
            background-attachment: fixed;
            background-position: center;
            background-size: cover;
        }

        /* --- DYNAMIC EFFECTS --- */
        .aurora-background { position: relative; }
        .aurora-background::before {
            content: '';
            position: fixed; /* Fixed position to cover viewport */
            top: 50%; left: 50%;
            width: 200vw; height: 200vh;
            background: radial-gradient(circle, rgba(59, 130, 246, 0.08) 0%, rgba(10, 10, 10, 0) 50%);
            transform: translate(-50%, -50%);
            animation: aurora 20s infinite linear;
            z-index: -1;
            pointer-events: none;
        }
        @keyframes aurora {
            0% { transform: translate(-50%, -50%) rotate(0deg); }
            100% { transform: translate(-50%, -50%) rotate(360deg); }
        }
        
        #home { position: relative; overflow: hidden; }
        #home::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            background: radial-gradient(circle 400px at var(--x, 50%) var(--y, 50%), rgba(255, 255, 255, 0.08), transparent 80%);
            pointer-events: none;
            transition: background 0.2s ease-out;
        }

        .text-gradient {
            background: linear-gradient(90deg, #a7c5ff, #ffffff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        /* Subtle text shadow for hero title to add depth */
        .hero-text-shadow {
             text-shadow: 0px 4px 15px rgba(0, 0, 0, 0.3);
        }

        .card-3d {
            transition: transform 0.4s ease, box-shadow 0.4s ease;
            transform-style: preserve-3d;
        }
        .card-3d:hover {
            transform: perspective(1000px) rotateY(var(--rotate-y, 0)) rotateX(var(--rotate-x, 0)) scale3d(1.05, 1.05, 1.05);
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
        }

        .gradient-border {
            position: relative;
            background: #111827; /* Card background */
            background-clip: padding-box;
            border: 2px solid transparent;
        }
        .gradient-border::before {
            content: '';
            position: absolute;
            top: 0; right: 0; bottom: 0; left: 0;
            z-index: -1; margin: -2px;
            border-radius: inherit;
            background: linear-gradient(145deg, rgba(59, 130, 246, 0.5), rgba(59, 130, 246, 0.1));
            opacity: 0;
            transition: opacity 0.3s ease-in-out;
        }
        .gradient-border:hover::before { opacity: 1; }
        
        .scroll-animate {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }
        .scroll-animate.is-visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* --- STATIC STYLING --- */
        .hero-gradient {
            background: linear-gradient(to top, #0A0A0A 8%, rgba(10, 10, 10, 0.7) 50%, rgba(10, 10, 10, 0.5) 75%), var(--bg-image);
            background-size: cover;
            background-position: center;
        }
        .cta-glow {
            box-shadow: 0 0 20px rgba(59, 130, 246, 0.5), 0 0 8px rgba(59, 130, 246, 0.7);
        }
        .recommended-card {
            transform: scale(1.05);
            border-color: #3b82f6;
        }
        .aspect-9-16 { position: relative; padding-top: 177.77%; }
        .aspect-9-16 > * { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }
        
        .lang-switcher .lang-option {
            cursor: pointer;
            transition: transform 0.2s ease;
        }
        .lang-switcher .lang-option:hover {
            transform: scale(1.1);
        }
        .lang-switcher .lang-option.active {
            border: 2px solid #3b82f6;
            transform: scale(1.1);
        }
        section {
            background-color: transparent;
        }

        /* Faster pulsating animation for the mobile menu icon */
        .pulsating-menu {
            animation: pulsate 0.5s infinite ease-in-out;
            border-radius: 50%;
        }
        @keyframes pulsate {
            0% {
                box-shadow: 0 0 0 0 rgba(59, 130, 246, 0.7);
            }
            70% {
                box-shadow: 0 0 0 10px rgba(59, 130, 246, 0);
            }
            100% {
                box-shadow: 0 0 0 0 rgba(59, 130, 246, 0);
            }
        }

        /* --- SCHEDULE STYLES --- */
        .filter-btn {
            transition: all 0.2s ease-in-out;
        }
        .filter-btn.active {
            background-color: #3b82f6;
            color: #ffffff;
            border-color: #3b82f6;
        }
        .schedule-item {
            transition: opacity 0.3s ease, transform 0.3s ease;
        }
    </style>
</head>
<body class="antialiased aurora-background pb-24 lg:pb-0">

    <!-- Header -->
    <header id="header" class="fixed top-0 left-0 right-0 z-50 transition-all duration-300 bg-black/30 backdrop-blur-md border-b border-white/10">
        <div class="container mx-auto px-4 sm:px-6">
            <div class="flex justify-between items-center py-4">
                <div class="flex-1 flex justify-start">
                    <a href="#home">
                        <!-- PERBAIKAN: Logo diperbesar untuk PC dan mobile -->
                        <img src="https://brandeps.com/logo-download/C/CNC-Fitness-logo-vector-01.svg" alt="CNC Fitness Logo" class="h-12 lg:h-14 w-auto">
                    </a>
                </div>
                
                <!-- Desktop Navigation (centered) -->
                <nav class="hidden lg:flex flex-auto justify-center items-center space-x-6">
                    <a href="#unggulan" class="text-gray-300 hover:text-white transition-colors" data-lang-key="navWhyUs">Keunggulan</a>
                    <a href="#pelatih" class="text-gray-300 hover:text-white transition-colors" data-lang-key="navTrainers">Pelatih</a>
                    <a href="#testimoni" class="text-gray-300 hover:text-white transition-colors" data-lang-key="navTestimonials">Testimoni</a>
                    <a href="#gallery" class="text-gray-300 hover:text-white transition-colors" data-lang-key="navGallery">Galeri</a>
                    <a href="#reels" class="text-gray-300 hover:text-white transition-colors" data-lang-key="navReels">Reels</a>
                    <a href="#jadwal" class="text-gray-300 hover:text-white transition-colors" data-lang-key="navSchedule">Jadwal</a>
                    <a href="#membership" class="text-gray-300 hover:text-white transition-colors" data-lang-key="navMembership">Membership</a>
                    <a href="https://www.google.com/maps/dir//CNC+Fitness+Pentacity" target="_blank" rel="noopener noreferrer" class="text-gray-300 hover:text-white transition-colors" data-lang-key="navLocation">Lokasi</a>
                    <a href="https://api.whatsapp.com/send?phone=6282191562827" target="_blank" rel="noopener noreferrer" class="text-gray-300 hover:text-white transition-colors" data-lang-key="navContact">Kontak</a>
                </nav>

                <!-- Header Controls: Language, CTA, Mobile Menu -->
                <div class="flex-1 flex justify-end items-center">
                    <div class="flex items-center space-x-3 sm:space-x-4">
                        <!-- PERBAIKAN: Kelas 'hidden' dihapus agar language switcher muncul di mobile -->
                        <div class="lang-switcher flex items-center space-x-2">
                            <img id="lang-id" src="https://flagcdn.com/id.svg" width="24" alt="Bahasa Indonesia" class="lang-option rounded-sm" title="Bahasa Indonesia" onerror="this.onerror=null;this.src='https://placehold.co/24x16';">
                            <img id="lang-en" src="https://flagcdn.com/gb.svg" width="24" alt="English" class="lang-option rounded-sm" title="English" onerror="this.onerror=null;this.src='https://placehold.co/24x16';">
                        </div>
                        <button id="mobile-menu-button" class="lg:hidden text-white focus:outline-none p-2 pulsating-menu">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
                            </svg>
                        </button>
                    </div>
                </div>
            </div>
        </div>
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden lg:hidden bg-gray-900/95 backdrop-blur-sm">
            <a href="#unggulan" class="mobile-link block text-center py-3 px-4 text-base text-gray-300 hover:bg-gray-800 transition-colors" data-lang-key="navWhyUs">Keunggulan</a>
            <a href="#pelatih" class="mobile-link block text-center py-3 px-4 text-base text-gray-300 hover:bg-gray-800 transition-colors" data-lang-key="navTrainers">Pelatih</a>
            <a href="#testimoni" class="mobile-link block text-center py-3 px-4 text-base text-gray-300 hover:bg-gray-800 transition-colors" data-lang-key="navTestimonials">Testimoni</a>
            <a href="#gallery" class="mobile-link block text-center py-3 px-4 text-base text-gray-300 hover:bg-gray-800 transition-colors" data-lang-key="navGallery">Galeri</a>
            <a href="#reels" class="mobile-link block text-center py-3 px-4 text-base text-gray-300 hover:bg-gray-800 transition-colors" data-lang-key="navReels">Reels</a>
            <a href="#jadwal" class="mobile-link block text-center py-3 px-4 text-base text-gray-300 hover:bg-gray-800 transition-colors" data-lang-key="navSchedule">Jadwal</a>
            <a href="#membership" class="mobile-link block text-center py-3 px-4 text-base text-gray-300 hover:bg-gray-800 transition-colors" data-lang-key="navMembership">Membership</a>
            <a href="https://www.google.com/maps/dir//CNC+Fitness+Pentacity" target="_blank" rel="noopener noreferrer" class="mobile-link block text-center py-3 px-4 text-base text-gray-300 hover:bg-gray-800 transition-colors" data-lang-key="navLocation">Lokasi</a>
            <a href="https://api.whatsapp.com/send?phone=6282191562827" target="_blank" rel="noopener noreferrer" class="mobile-link block text-center py-3 px-4 text-base text-gray-300 hover:bg-gray-800 transition-colors" data-lang-key="navContact">Kontak</a>
        </div>
    </header>

    <main class="relative z-10">
        <!-- Hero Section -->
        <section id="home"
            style="--bg-image: url('https://images.unsplash.com/photo-1581009146145-b5ef050c2e1e?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3');"
            class="relative min-h-screen flex items-center justify-center text-center hero-gradient text-white pt-20">
            <div class="container mx-auto px-4 sm:px-6 relative z-10 scroll-animate">
                <h1 class="text-4xl sm:text-5xl md:text-7xl lg:text-8xl font-black uppercase tracking-wide leading-tight hero-text-shadow" data-lang-key="heroTitle">
                    Capai Target <span class="text-gradient">Kebugaran</span> Anda
                </h1>
                <p class="mt-6 text-base sm:text-lg md:text-xl max-w-3xl mx-auto text-gray-300" data-lang-key="heroSubtitle">
                    CNC Fitness BSB menyediakan fasilitas premium, pelatih ahli, dan komunitas yang mendukung untuk membantu Anda meraih hasil nyata.
                </p>
                <div class="mt-10">
                    <a href="#membership" class="bg-blue-600 text-white font-bold text-base sm:text-lg px-8 py-3 sm:px-10 sm:py-4 rounded-lg hover:bg-blue-500 transition-all duration-300 inline-block cta-glow" data-lang-key="heroCTA">
                        Lihat Paket Membership
                    </a>
                </div>
            </div>
        </section>

        <!-- Why Us Section -->
        <section id="unggulan" class="py-16 sm:py-24">
            <div class="container mx-auto px-4 sm:px-6">
                <div class="text-center mb-12 sm:mb-16 scroll-animate">
                    <h2 class="text-3xl md:text-4xl font-bold text-white" data-lang-key="whyUsTitle">Kenapa Berlatih di CNC Fitness?</h2>
                    <p class="mt-3 max-w-2xl mx-auto text-gray-400" data-lang-key="whyUsSubtitle">Kami menyediakan semua yang Anda butuhkan untuk mendukung perjalanan kebugaran Anda.</p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 sm:gap-8">
                    <div class="p-6 sm:p-8 rounded-xl gradient-border card-3d scroll-animate" style="transition-delay: 100ms;">
                        <div class="text-blue-400 mb-4">
                            <!-- PERBAIKAN: Ikon diganti menjadi barbel -->
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                              <path stroke-linecap="round" stroke-linejoin="round" d="M2 12h2m16 0h2M5 12h14" />
                              <path stroke-linecap="round" stroke-linejoin="round" d="M5 7v10h2V7H5zm12 0v10h2V7h-2z" />
                            </svg>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-2" data-lang-key="feature1Title">Peralatan Terbaik</h3>
                        <p class="text-gray-400" data-lang-key="feature1Desc">Akses ke peralatan fitness modern untuk latihan yang lebih efektif dan terukur.</p>
                    </div>
                    <div class="p-6 sm:p-8 rounded-xl gradient-border card-3d scroll-animate" style="transition-delay: 200ms;">
                        <div class="text-blue-400 mb-4">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"></path><circle cx="8.5" cy="7" r="4"></circle><polyline points="17 11 19 13 23 9"></polyline></svg>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-2" data-lang-key="feature2Title">Pelatih Profesional</h3>
                        <p class="text-gray-400" data-lang-key="feature2Desc">Dapatkan panduan dari tim pelatih bersertifikasi untuk program latihan yang aman dan personal.</p>
                    </div>
                    <div class="p-6 sm:p-8 rounded-xl gradient-border card-3d scroll-animate" style="transition-delay: 300ms;">
                        <div class="text-blue-400 mb-4">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m18 13-2.5 2.5a4.24 4.24 0 0 1-6 0L7 13l-2.5 2.5a4.24 4.24 0 0 0 6 0L13 13l2.5-2.5a4.24 4.24 0 0 1 6 0L19 13l2.5-2.5a4.24 4.24 0 0 0-6 0L13 13"></path></svg>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-2" data-lang-key="feature3Title">Kelas Beragam</h3>
                        <p class="text-gray-400" data-lang-key="feature3Desc">Jaga motivasi Anda dengan berbagai pilihan kelas, dari Yoga hingga HIIT yang intens.</p>
                    </div>
                    <div class="p-6 sm:p-8 rounded-xl gradient-border card-3d scroll-animate" style="transition-delay: 400ms;">
                        <div class="text-blue-400 mb-4">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2L2 7l10 5 10-5-10-5z"></path><path d="M2 17l10 5 10-5"></path><path d="M2 12l10 5 10-5"></path></svg>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-2" data-lang-key="feature4Title">Fasilitas Premium</h3>
                        <p class="text-gray-400" data-lang-key="feature4Desc">Nikmati lingkungan eksklusif, dilengkapi sauna, lounge, dan ruang ganti yang nyaman.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Trainers Section -->
        <section id="pelatih" class="py-16 sm:py-24">
            <div class="container mx-auto px-4 sm:px-6">
                <div class="text-center mb-12 sm:mb-16 scroll-animate">
                    <h2 class="text-3xl md:text-4xl font-bold text-white" data-lang-key="trainersTitle">Temui Tim Pelatih Profesional Kami</h2>
                    <p class="mt-3 max-w-2xl mx-auto text-gray-400" data-lang-key="trainersSubtitle">Berlatih lebih cerdas dengan bimbingan dari para ahli kebugaran.</p>
                </div>
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8 sm:gap-10">
                    <div class="rounded-xl overflow-hidden text-center group card-3d scroll-animate" style="transition-delay: 100ms;">
                        <div class="gradient-border rounded-xl">
                            <img src="https://placehold.co/400x500/3b82f6/FFFFFF?text=Foto+Pelatih+1" alt="Pelatih Profesional CNC Fitness 1" class="w-full h-80 object-cover group-hover:scale-105 transition-transform duration-300 rounded-t-xl" onerror="this.onerror=null;this.src='https://placehold.co/400x500';">
                            <div class="p-6">
                                <h3 class="text-2xl font-bold text-white" data-lang-key="trainer1Name">Andi Setiawan</h3>
                                <p class="text-blue-400 font-semibold mt-1" data-lang-key="trainer1Spec">Kekuatan & Kondisi</p>
                                <p class="text-gray-400 mt-3 text-sm" data-lang-key="trainer1Desc">Ahli merancang program kekuatan untuk meningkatkan performa dan membentuk postur ideal.</p>
                            </div>
                        </div>
                    </div>
                    <div class="rounded-xl overflow-hidden text-center group card-3d scroll-animate" style="transition-delay: 200ms;">
                        <div class="gradient-border rounded-xl">
                            <img src="https://placehold.co/400x500/111827/FFFFFF?text=Foto+Pelatih+2" alt="Pelatih Profesional CNC Fitness 2" class="w-full h-80 object-cover group-hover:scale-105 transition-transform duration-300 rounded-t-xl" onerror="this.onerror=null;this.src='https://placehold.co/400x500';">
                            <div class="p-6">
                                <h3 class="text-2xl font-bold text-white" data-lang-key="trainer2Name">Citra Amelia</h3>
                                <p class="text-blue-400 font-semibold mt-1" data-lang-key="trainer2Spec">Penurunan Berat Badan & Nutrisi</p>
                                <p class="text-gray-400 mt-3 text-sm" data-lang-key="trainer2Desc">Memadukan latihan efektif dengan panduan nutrisi untuk membantu Anda mencapai berat badan ideal.</p>
                            </div>
                        </div>
                    </div>
                    <div class="rounded-xl overflow-hidden text-center group card-3d scroll-animate" style="transition-delay: 300ms;">
                        <div class="gradient-border rounded-xl">
                            <img src="https://placehold.co/400x500/3b82f6/FFFFFF?text=Foto+Pelatih+3" alt="Pelatih Profesional CNC Fitness 3" class="w-full h-80 object-cover group-hover:scale-105 transition-transform duration-300 rounded-t-xl" onerror="this.onerror=null;this.src='https://placehold.co/400x500';">
                            <div class="p-6">
                                <h3 class="text-2xl font-bold text-white" data-lang-key="trainer3Name">David Lee</h3>
                                <p class="text-blue-400 font-semibold mt-1" data-lang-key="trainer3Spec">Fungsional & Mobilitas</p>
                                <p class="text-gray-400 mt-3 text-sm" data-lang-key="trainer3Desc">Spesialis latihan fungsional untuk meningkatkan mobilitas dan kekuatan untuk aktivitas sehari-hari.</p>
                            </div>
                        </div>
                    </div>
                    <div class="rounded-xl overflow-hidden text-center group card-3d scroll-animate" style="transition-delay: 400ms;">
                        <div class="gradient-border rounded-xl">
                            <img src="https://placehold.co/400x500/111827/FFFFFF?text=Foto+Pelatih+4" alt="Pelatih Profesional CNC Fitness 4" class="w-full h-80 object-cover group-hover:scale-105 transition-transform duration-300 rounded-t-xl" onerror="this.onerror=null;this.src='https://placehold.co/400x500';">
                            <div class="p-6">
                                <h3 class="text-2xl font-bold text-white" data-lang-key="trainer4Name">Sari Wulandari</h3>
                                <p class="text-blue-400 font-semibold mt-1" data-lang-key="trainer4Spec">Yoga & Fleksibilitas</p>
                                <p class="text-gray-400 mt-3 text-sm" data-lang-key="trainer4Desc">Membantu Anda menemukan ketenangan dan meningkatkan kelenturan tubuh melalui yoga.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Testimonials Section -->
        <section id="testimoni" class="py-16 sm:py-24">
            <div class="container mx-auto px-4 sm:px-6">
                <div class="text-center mb-12 sm:mb-16 scroll-animate">
                    <h2 class="text-3xl md:text-4xl font-bold text-white" data-lang-key="testimonialsTitle">Kata Mereka Tentang Kami</h2>
                    <p class="mt-3 max-w-2xl mx-auto text-gray-400" data-lang-key="testimonialsSubtitle">Kisah sukses nyata dari para member kami yang luar biasa.</p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Testimonial Card 1 -->
                    <div class="p-8 rounded-xl gradient-border card-3d scroll-animate flex flex-col" style="transition-delay: 100ms;">
                        <div class="flex-grow">
                            <div class="flex items-center mb-4">
                                <img src="https://placehold.co/64x64/3b82f6/FFFFFF?text=A" class="w-16 h-16 rounded-full object-cover border-2 border-blue-500" alt="Foto Member 1" onerror="this.onerror=null;this.src='https://placehold.co/64x64';">
                                <div class="ml-4">
                                    <h4 class="text-lg font-bold text-white" data-lang-key="testi1Name">Ahmad Prasetyo</h4>
                                    <div class="flex text-yellow-400 mt-1">
                                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                    </div>
                                    <!-- PERBAIKAN: Tanggal ditambahkan -->
                                    <p class="text-xs text-gray-500 mt-2" data-lang-key="testi1Date"></p>
                                </div>
                            </div>
                            <p class="text-gray-300 italic" data-lang-key="testi1Quote">"Fasilitasnya luar biasa dan para pelatihnya sangat profesional. Saya berhasil mencapai target berat badan saya dalam 3 bulan. Sangat direkomendasikan!"</p>
                        </div>
                    </div>
                    <!-- Testimonial Card 2 -->
                    <div class="p-8 rounded-xl gradient-border card-3d scroll-animate flex flex-col" style="transition-delay: 200ms;">
                       <div class="flex-grow">
                            <div class="flex items-center mb-4">
                                <img src="https://placehold.co/64x64/111827/FFFFFF?text=S" class="w-16 h-16 rounded-full object-cover border-2 border-blue-500" alt="Foto Member 2" onerror="this.onerror=null;this.src='https://placehold.co/64x64';">
                                <div class="ml-4">
                                    <h4 class="text-lg font-bold text-white" data-lang-key="testi2Name">Siti Nurhaliza</h4>
                                    <div class="flex text-yellow-400 mt-1">
                                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                    </div>
                                    <!-- PERBAIKAN: Tanggal ditambahkan -->
                                    <p class="text-xs text-gray-500 mt-2" data-lang-key="testi2Date"></p>
                                </div>
                            </div>
                            <p class="text-gray-300 italic" data-lang-key="testi2Quote">"Kelas Yoga di sini adalah yang terbaik di Balikpapan. Instrukturnya sabar dan lingkungannya sangat mendukung. Saya merasa lebih bugar dan tenang."</p>
                        </div>
                    </div>
                    <!-- Testimonial Card 3 -->
                    <div class="p-8 rounded-xl gradient-border card-3d scroll-animate flex flex-col" style="transition-delay: 300ms;">
                        <div class="flex-grow">
                            <div class="flex items-center mb-4">
                                <img src="https://placehold.co/64x64/3b82f6/FFFFFF?text=B" class="w-16 h-16 rounded-full object-cover border-2 border-blue-500" alt="Foto Member 3" onerror="this.onerror=null;this.src='https://placehold.co/64x64';">
                                <div class="ml-4">
                                    <h4 class="text-lg font-bold text-white" data-lang-key="testi3Name">Budi Santoso</h4>
                                    <div class="flex text-yellow-400 mt-1">
                                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                    </div>
                                    <!-- PERBAIKAN: Tanggal ditambahkan -->
                                    <p class="text-xs text-gray-500 mt-2" data-lang-key="testi3Date"></p>
                                </div>
                            </div>
                            <p class="text-gray-300 italic" data-lang-key="testi3Quote">"Komunitas di CNC Fitness sangat positif. Saya tidak hanya mendapatkan tubuh yang lebih sehat, tetapi juga teman-teman baru yang memiliki semangat yang sama."</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Gallery Section -->
        <section id="gallery" class="py-16 sm:py-24">
            <div class="container mx-auto px-4 sm:px-6">
                <div class="text-center mb-12 sm:mb-16 scroll-animate">
                    <h2 class="text-3xl md:text-4xl font-bold text-white" data-lang-key="galleryTitle">Galeri CNC Fitness</h2>
                    <p class="mt-3 max-w-2xl mx-auto text-gray-400" data-lang-key="gallerySubtitle">Lihat lebih dekat suasana dan fasilitas kami.</p>
                </div>
                <div class="grid grid-cols-2 md:grid-cols-3 gap-3 sm:gap-4">
                    <div class="group scroll-animate"><img class="h-auto w-full rounded-lg object-cover group-hover:scale-105 transition-transform duration-300" src="https://placehold.co/800x600/111827/FFFFFF?text=Suasana+Latihan" alt="Suasana latihan di CNC Fitness" onerror="this.onerror=null;this.src='https://placehold.co/800x600';"></div>
                    <div class="group scroll-animate" style="transition-delay: 100ms;"><img class="h-auto w-full rounded-lg object-cover group-hover:scale-105 transition-transform duration-300" src="https://placehold.co/800x600/3b82f6/FFFFFF?text=Sesi+Personal+Trainer" alt="Sesi Personal Trainer" onerror="this.onerror=null;this.src='https://placehold.co/800x600';"></div>
                    <div class="group scroll-animate" style="transition-delay: 200ms;"><img class="h-auto w-full rounded-lg object-cover group-hover:scale-105 transition-transform duration-300" src="https://placehold.co/800x600/111827/FFFFFF?text=Kelas+Zumba" alt="Kelas Zumba yang energik" onerror="this.onerror=null;this.src='https://placehold.co/800x600';"></div>
                    <div class="group scroll-animate" style="transition-delay: 300ms;"><img class="h-auto w-full rounded-lg object-cover group-hover:scale-105 transition-transform duration-300" src="https://placehold.co/800x600/3b82f6/FFFFFF?text=Area+Angkat+Beban" alt="Area angkat beban yang lengkap" onerror="this.onerror=null;this.src='https://placehold.co/800x600';"></div>
                    <div class="group scroll-animate" style="transition-delay: 400ms;"><img class="h-auto w-full rounded-lg object-cover group-hover:scale-105 transition-transform duration-300" src="https://placehold.co/800x600/111827/FFFFFF?text=Detail+Fasilitas" alt="Detail fasilitas premium" onerror="this.onerror=null;this.src='https://placehold.co/800x600';"></div>
                    <div class="group scroll-animate" style="transition-delay: 500ms;"><img class="h-auto w-full rounded-lg object-cover group-hover:scale-105 transition-transform duration-300" src="https://placehold.co/800x600/3b82f6/FFFFFF?text=Komunitas+Member" alt="Komunitas member CNC Fitness" onerror="this.onerror=null;this.src='https://placehold.co/800x600';"></div>
                </div>
            </div>
        </section>

        <!-- Equipment Gallery Section -->
        <section id="equipment-gallery" class="py-16 sm:py-24">
            <div class="container mx-auto px-4 sm:px-6">
                <div class="text-center mb-12 sm:mb-16 scroll-animate">
                    <h2 class="text-3xl md:text-4xl font-bold text-white" data-lang-key="equipmentTitle">Galeri Peralatan</h2>
                    <p class="mt-3 max-w-2xl mx-auto text-gray-400" data-lang-key="equipmentSubtitle">Peralatan modern dan lengkap untuk setiap kebutuhan latihan Anda.</p>
                </div>
                <div class="grid grid-cols-2 md:grid-cols-4 gap-3 sm:gap-4">
                    <div class="group scroll-animate"><img class="h-auto w-full rounded-lg object-cover" src="https://placehold.co/600x600/3b82f6/FFFFFF?text=Cardio+Line" alt="Cardio Line" onerror="this.onerror=null;this.src='https://placehold.co/600x600';"></div>
                    <div class="group scroll-animate" style="transition-delay: 100ms;"><img class="h-auto w-full rounded-lg object-cover" src="https://placehold.co/600x600/111827/FFFFFF?text=Dumbbell+Rack" alt="Dumbbell Rack" onerror="this.onerror=null;this.src='https://placehold.co/600x600';"></div>
                    <div class="group scroll-animate" style="transition-delay: 200ms;"><img class="h-auto w-full rounded-lg object-cover" src="https://placehold.co/600x600/3b82f6/FFFFFF?text=Smith+Machine" alt="Smith Machine" onerror="this.onerror=null;this.src='https://placehold.co/600x600';"></div>
                    <div class="group scroll-animate" style="transition-delay: 300ms;"><img class="h-auto w-full rounded-lg object-cover" src="https://placehold.co/600x600/111827/FFFFFF?text=Functional+Area" alt="Functional Area" onerror="this.onerror=null;this.src='https://placehold.co/600x600';"></div>
                    <div class="group scroll-animate" style="transition-delay: 400ms;"><img class="h-auto w-full rounded-lg object-cover" src="https://placehold.co/600x600/3b82f6/FFFFFF?text=Leg+Press+Machine" alt="Leg Press Machine" onerror="this.onerror=null;this.src='https://placehold.co/600x600';"></div>
                    <div class="group scroll-animate" style="transition-delay: 500ms;"><img class="h-auto w-full rounded-lg object-cover" src="https://placehold.co/600x600/111827/FFFFFF?text=Cable+Crossover" alt="Cable Crossover" onerror="this.onerror=null;this.src='https://placehold.co/600x600';"></div>
                </div>
            </div>
        </section>

        <!-- Reels Section -->
        <section id="reels" class="py-16 sm:py-24">
            <div class="container mx-auto px-4 sm:px-6">
                <div class="text-center mb-12 sm:mb-16 scroll-animate">
                    <h2 class="text-3xl md:text-4xl font-bold text-white" data-lang-key="reelsTitle">Aksi Nyata, Hasil Nyata</h2>
                    <p class="mt-3 max-w-2xl mx-auto text-gray-400" data-lang-key="reelsSubtitle">Lihat energi dan komunitas kami melalui Reels terbaru di Instagram.</p>
                </div>
                <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 gap-3 sm:gap-4">
                    <a href="https://www.instagram.com/cncfitnessbsb/reels/" target="_blank" rel="noopener noreferrer" class="group block rounded-lg overflow-hidden reel-item aspect-9-16 scroll-animate" style="transition-delay: 100ms;"><img src="https://placehold.co/360x640/111827/FFFFFF?text=CNC+Reel+1" alt="Instagram Reel 1" class="object-cover transition-transform duration-300 group-hover:scale-110" onerror="this.onerror=null;this.src='https://placehold.co/360x640';"><div class="flex items-center justify-center bg-black bg-opacity-20 group-hover:bg-opacity-40 transition-all duration-300"><svg class="w-16 h-16 text-white opacity-80 group-hover:opacity-100 group-hover:scale-110 transition-all duration-300" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM9.555 7.168A1 1 0 008 8v4a1 1 0 001.555.832l3-2a1 1 0 000-1.664l-3-2z" clip-rule="evenodd"></path></svg></div></a>
                    <a href="https://www.instagram.com/cncfitnessbsb/reels/" target="_blank" rel="noopener noreferrer" class="group block rounded-lg overflow-hidden reel-item aspect-9-16 scroll-animate" style="transition-delay: 200ms;"><img src="https://placehold.co/360x640/3b82f6/FFFFFF?text=CNC+Reel+2" alt="Instagram Reel 2" class="object-cover transition-transform duration-300 group-hover:scale-110" onerror="this.onerror=null;this.src='https://placehold.co/360x640';"><div class="flex items-center justify-center bg-black bg-opacity-20 group-hover:bg-opacity-40 transition-all duration-300"><svg class="w-16 h-16 text-white opacity-80 group-hover:opacity-100 group-hover:scale-110 transition-all duration-300" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM9.555 7.168A1 1 0 008 8v4a1 1 0 001.555.832l3-2a1 1 0 000-1.664l-3-2z" clip-rule="evenodd"></path></svg></div></a>
                    <a href="https://www.instagram.com/cncfitnessbsb/reels/" target="_blank" rel="noopener noreferrer" class="group block rounded-lg overflow-hidden reel-item aspect-9-16 scroll-animate" style="transition-delay: 300ms;"><img src="https://placehold.co/360x640/111827/FFFFFF?text=CNC+Reel+3" alt="Instagram Reel 3" class="object-cover transition-transform duration-300 group-hover:scale-110" onerror="this.onerror=null;this.src='https://placehold.co/360x640';"><div class="flex items-center justify-center bg-black bg-opacity-20 group-hover:bg-opacity-40 transition-all duration-300"><svg class="w-16 h-16 text-white opacity-80 group-hover:opacity-100 group-hover:scale-110 transition-all duration-300" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM9.555 7.168A1 1 0 008 8v4a1 1 0 001.555.832l3-2a1 1 0 000-1.664l-3-2z" clip-rule="evenodd"></path></svg></div></a>
                    <a href="https://www.instagram.com/cncfitnessbsb/reels/" target="_blank" rel="noopener noreferrer" class="group block rounded-lg overflow-hidden reel-item aspect-9-16 scroll-animate" style="transition-delay: 400ms;"><img src="https://placehold.co/360x640/3b82f6/FFFFFF?text=CNC+Reel+4" alt="Instagram Reel 4" class="object-cover transition-transform duration-300 group-hover:scale-110" onerror="this.onerror=null;this.src='https://placehold.co/360x640';"><div class="flex items-center justify-center bg-black bg-opacity-20 group-hover:bg-opacity-40 transition-all duration-300"><svg class="w-16 h-16 text-white opacity-80 group-hover:opacity-100 group-hover:scale-110 transition-all duration-300" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM9.555 7.168A1 1 0 008 8v4a1 1 0 001.555.832l3-2a1 1 0 000-1.664l-3-2z" clip-rule="evenodd"></path></svg></div></a>
                </div>
                 <div class="text-center mt-12 scroll-animate">
                    <a href="https://www.instagram.com/cncfitnessbsb/reels/" target="_blank" rel="noopener noreferrer" class="bg-blue-600 text-white font-semibold px-8 py-3 rounded-lg hover:bg-blue-500 transition-all duration-300" data-lang-key="reelsCTA">
                        Lihat Semua Reels
                    </a>
                </div>
            </div>
        </section>

        <!-- Schedule Section -->
        <section id="jadwal" class="py-16 sm:py-24">
            <div class="container mx-auto px-4 sm:px-6">
                <div class="text-center mb-12 sm:mb-16 scroll-animate">
                    <h2 class="text-3xl md:text-4xl font-bold text-white" data-lang-key="scheduleTitle">Jadwal Kelas Interaktif</h2>
                    <p class="mt-3 max-w-2xl mx-auto text-gray-400" data-lang-key="scheduleSubtitle">Filter berdasarkan hari atau tipe kelas untuk menemukan sesi yang sempurna untuk Anda.</p>
                </div>
                
                <div id="schedule-filters" class="flex flex-wrap justify-center items-center gap-2 sm:gap-3 mb-10 scroll-animate">
                    <button class="filter-btn active border border-blue-500 px-4 py-2 rounded-full text-sm font-semibold" data-filter="all" data-lang-key="filterAll">Semua</button>
                    <button class="filter-btn border border-gray-600 text-gray-300 hover:bg-gray-700 px-4 py-2 rounded-full text-sm font-semibold" data-filter="senin" data-lang-key="filterMonday">Senin</button>
                    <button class="filter-btn border border-gray-600 text-gray-300 hover:bg-gray-700 px-4 py-2 rounded-full text-sm font-semibold" data-filter="selasa" data-lang-key="filterTuesday">Selasa</button>
                    <button class="filter-btn border border-gray-600 text-gray-300 hover:bg-gray-700 px-4 py-2 rounded-full text-sm font-semibold" data-filter="rabu" data-lang-key="filterWednesday">Rabu</button>
                    <button class="filter-btn border border-gray-600 text-gray-300 hover:bg-gray-700 px-4 py-2 rounded-full text-sm font-semibold" data-filter="kamis" data-lang-key="filterThursday">Kamis</button>
                    <button class="filter-btn border border-gray-600 text-gray-300 hover:bg-gray-700 px-4 py-2 rounded-full text-sm font-semibold" data-filter="jumat" data-lang-key="filterFriday">Jumat</button>
                    <span class="w-full sm:w-auto text-center my-2 sm:my-0 text-gray-500 mx-2">|</span>
                    <button class="filter-btn border border-gray-600 text-gray-300 hover:bg-gray-700 px-4 py-2 rounded-full text-sm font-semibold" data-filter="yoga" data-lang-key="filterYoga">Yoga</button>
                    <button class="filter-btn border border-gray-600 text-gray-300 hover:bg-gray-700 px-4 py-2 rounded-full text-sm font-semibold" data-filter="hiit" data-lang-key="filterHiit">HIIT</button>
                    <button class="filter-btn border border-gray-600 text-gray-300 hover:bg-gray-700 px-4 py-2 rounded-full text-sm font-semibold" data-filter="strength" data-lang-key="filterStrength">Strength</button>
                </div>

                <div id="schedule-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                    <!-- Jadwal akan diisi oleh JavaScript -->
                </div>
            </div>
        </section>

        <!-- Membership Section -->
        <section id="membership" class="py-16 sm:py-24">
            <div class="container mx-auto px-4 sm:px-6">
                <div class="text-center mb-12 sm:mb-16 scroll-animate">
                    <h2 class="text-3xl md:text-4xl font-bold text-white" data-lang-key="membershipTitle">Investasi Untuk Diri Anda</h2>
                    <p class="mt-3 max-w-2xl mx-auto text-gray-400" data-lang-key="membershipSubtitle">Pilih paket yang paling sesuai dengan gaya hidup dan tujuan Anda. Komitmen kami adalah transparansi penuh.</p>
                </div>
                <div class="flex flex-wrap justify-center items-stretch gap-8">
                    <div class="w-full max-w-sm p-6 sm:p-8 rounded-xl transition-all duration-300 card-3d gradient-border scroll-animate flex flex-col" style="transition-delay: 100ms;">
                        <div class="flex-grow">
                            <h3 class="text-xl font-semibold text-white" data-lang-key="plan1Title">1 Bulan</h3>
                            <p class="mt-1 text-gray-400" data-lang-key="plan1Subtitle">Fleksibel & Cepat</p>
                            <p class="mt-6 text-4xl font-bold text-white" data-lang-key="plan1Price">Rp 550.000</p>
                            <ul class="mt-6 space-y-3 text-gray-300">
                                <li class="flex items-center" data-lang-key="planFeatureAllAccess"><svg class="w-5 h-5 text-blue-500 mr-2 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>Akses semua alat</li>
                                <li class="flex items-center" data-lang-key="planFeatureClassAccess"><svg class="w-5 h-5 text-blue-500 mr-2 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>Akses semua kelas</li>
                                <li class="flex items-center" data-lang-key="planFeatureTowel"><svg class="w-5 h-5 text-blue-500 mr-2 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>Handuk & Loker</li>
                            </ul>
                        </div>
                        <a href="#" data-wa-key="plan1" target="_blank" rel="noopener noreferrer" class="mt-8 block w-full text-center bg-gray-700 text-white font-semibold py-3 rounded-lg hover:bg-gray-600 transition-colors" data-lang-key="planCTA">Pilih Paket</a>
                    </div>

                    <div class="w-full max-w-sm p-6 sm:p-8 rounded-xl transition-all duration-300 relative card-3d gradient-border recommended-card scroll-animate flex flex-col" style="transition-delay: 200ms;">
                        <div class="flex-grow">
                            <span class="absolute top-0 -translate-y-1/2 left-1/2 -translate-x-1/2 bg-blue-600 text-white text-xs font-bold px-4 py-1 rounded-full" data-lang-key="planPopular">Paling Populer</span>
                            <h3 class="text-xl font-semibold text-white" data-lang-key="plan2Title">6 Bulan</h3>
                            <p class="mt-1 text-gray-400" data-lang-key="plan2Subtitle">Komitmen & Hasil</p>
                            <p class="mt-6 text-4xl font-bold text-white" data-lang-key="plan2Price">Rp 2.750.000</p>
                            <p class="text-sm text-gray-400" data-lang-key="plan2Save">Hemat Rp 550.000</p>
                            <ul class="mt-6 space-y-3 text-gray-300">
                                <li class="flex items-center" data-lang-key="plan2Feature1"><svg class="w-5 h-5 text-blue-500 mr-2 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>Semua di paket 1 Bulan</li>
                                <li class="flex items-center font-bold" data-lang-key="plan2Feature2"><svg class="w-5 h-5 text-blue-500 mr-2 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>1x Sesi Personal Trainer</li>
                                <li class="flex items-center font-bold" data-lang-key="plan2Feature3"><svg class="w-5 h-5 text-blue-500 mr-2 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>Analisa Komposisi Tubuh</li>
                            </ul>
                        </div>
                        <a href="#" data-wa-key="plan2" target="_blank" rel="noopener noreferrer" class="mt-8 block w-full text-center bg-blue-600 text-white font-semibold py-3 rounded-lg hover:bg-blue-500 transition-colors" data-lang-key="planCTA">Pilih Paket</a>
                    </div>

                    <div class="w-full max-w-sm p-6 sm:p-8 rounded-xl transition-all duration-300 card-3d gradient-border scroll-animate flex flex-col" style="transition-delay: 300ms;">
                        <div class="flex-grow">
                            <h3 class="text-xl font-semibold text-white" data-lang-key="plan3Title">12 Bulan</h3>
                            <p class="mt-1 text-gray-400" data-lang-key="plan3Subtitle">Transformasi Total</p>
                            <p class="mt-6 text-4xl font-bold text-white" data-lang-key="plan3Price">Rp 4.950.000</p>
                            <p class="text-sm text-gray-400" data-lang-key="plan3Save">Hemat Rp 1.650.000</p>
                            <ul class="mt-6 space-y-3 text-gray-300">
                                <li class="flex items-center" data-lang-key="plan3Feature1"><svg class="w-5 h-5 text-blue-500 mr-2 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>Semua di paket 6 Bulan</li>
                                <li class="flex items-center font-bold" data-lang-key="plan3Feature2"><svg class="w-5 h-5 text-blue-500 mr-2 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>Merchandise Eksklusif</li>
                                <li class="flex items-center font-bold" data-lang-key="plan3Feature3"><svg class="w-5 h-5 text-blue-500 mr-2 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>Konsultasi Nutrisi</li>
                            </ul>
                        </div>
                        <a href="#" data-wa-key="plan3" target="_blank" rel="noopener noreferrer" class="mt-8 block w-full text-center bg-gray-700 text-white font-semibold py-3 rounded-lg hover:bg-gray-600 transition-colors" data-lang-key="planCTA">Pilih Paket</a>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- CTA Trial Section -->
        <section id="cta-trial" class="bg-blue-600/80">
            <div class="container mx-auto px-4 sm:px-6 py-16 text-center scroll-animate">
                <h2 class="text-3xl font-bold text-white" data-lang-key="trialTitle">Siap Memulai Perjalanan Anda?</h2>
                <p class="mt-2 text-blue-100 max-w-xl mx-auto" data-lang-key="trialSubtitle">Dapatkan <span class="font-bold">Free Trial 1 Hari</span> untuk merasakan sendiri pengalaman premium di CNC Fitness. Klaim sekarang!</p>
                <a href="#" data-wa-key="trial" target="_blank" rel="noopener noreferrer" class="mt-6 inline-block bg-white text-blue-600 font-bold px-8 py-3 rounded-lg hover:bg-gray-200 transition-colors" data-lang-key="trialCTA">Klaim Free Trial via WhatsApp</a>
            </div>
        </section>

        <!-- Location Section -->
        <section id="lokasi" class="py-16 sm:py-24">
            <div class="container mx-auto px-4 sm:px-6 grid md:grid-cols-2 gap-12 items-center scroll-animate">
                <div>
                    <h2 class="text-3xl md:text-4xl font-bold text-white" data-lang-key="locationTitle">Pusat Kebugaran Premium di Balikpapan</h2>
                    <p class="mt-4 text-gray-400" data-lang-key="locationSubtitle">Lokasi kami yang strategis di Balikpapan Superblock memudahkan Anda untuk berolahraga kapan saja.</p>
                    <div class="mt-6 space-y-4">
                        <div class="flex items-start">
                            <svg class="w-6 h-6 text-blue-500 mr-3 mt-1 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path></svg>
                            <span data-lang-key="locationAddress">Balikpapan Superblock, Pentacity Shopping Venue, Lt. 2<br>Jl. Jenderal Sudirman No. 47, Balikpapan, Kalimantan Timur</span>
                        </div>
                        <div class="flex items-center">
                            <svg class="w-6 h-6 text-blue-500 mr-3 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path></svg>
                            <span>(0542) 8527805</span>
                        </div>
                        <div class="flex items-center">
                            <svg class="w-7 h-7 text-green-500 mr-2.5 flex-shrink-0" fill="currentColor" viewBox="0 0 24 24"><path d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.946.003-6.556 5.338-11.891 11.893-11.891 3.181.001 6.167 1.24 8.413 3.488 2.245 2.248 3.481 5.236 3.48 8.414-.003 6.557-5.338 11.892-11.893 11.892-1.99-.001-3.951-.5-5.688-1.448l-6.305 1.654zm6.597-3.807c1.676.995 3.276 1.591 5.392 1.592 5.448 0 9.886-4.434 9.889-9.885.002-5.462-4.415-9.89-9.881-9.892-5.452 0-9.887 4.434-9.889 9.884-.001 2.225.651 4.315 1.731 6.086l.001.004 4.971 4.971z"/></svg>
                            <a href="https://api.whatsapp.com/send?phone=6282191562827" target="_blank" rel="noopener noreferrer" class="hover:text-white transition-colors" data-lang-key="locationWhatsapp">0821-9156-2827</a>
                        </div>
                        <div class="flex items-start">
                            <svg class="w-6 h-6 text-blue-500 mr-3 mt-1 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                            <span data-lang-key="locationHours">Senin - Sabtu: 06:00 - 22:00 | Minggu: 08:00 - 20:00</span>
                        </div>
                    </div>
                </div>
                <!-- Updated Map: Replaced image with interactive iframe -->
                <div class="rounded-lg overflow-hidden shadow-2xl h-80 md:h-full">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3988.832239474158!2d116.8546503153941!3d-1.274174099071031!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2df1477c9597a235%3A0x6e1c3669972cd63f!2sCNC%20Fitness%20Pentacity!5e0!3m2!1sen!2sid!4v1678886453215!5m2!1sen!2sid" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade" class="w-full h-full"></iframe>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-transparent border-t border-gray-800">
        <div class="container mx-auto px-4 sm:px-6 py-8 text-center text-gray-400">
            <p data-lang-key="footerRights">© 2025 CNC Fitness BSB. All Rights Reserved.</p>
            <div class="flex justify-center space-x-6 mt-4">
                <a href="https://www.instagram.com/cncfitnessbsb/" target="_blank" rel="noopener noreferrer" class="hover:opacity-80 transition-opacity" aria-label="Instagram">
                    <svg class="h-7 w-7" viewBox="0 0 24 24">
                        <defs><radialGradient id="ig-gradient" gradientUnits="userSpaceOnUse" cx="8.21" cy="19.34" r="22.38"><stop offset="0" stop-color="#fdd87d"/><stop offset=".1" stop-color="#fdd87d"/><stop offset=".25" stop-color="#fca667"/><stop offset=".4" stop-color="#f8775f"/><stop offset=".5" stop-color="#f45c61"/><stop offset=".6" stop-color="#d73379"/><stop offset=".75" stop-color="#b62a99"/><stop offset=".9" stop-color="#9d2fbc"/><stop offset="1" stop-color="#8c33c4"/></radialGradient></defs>
                        <path fill="url(#ig-gradient)" d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.85s-.012 3.584-.07 4.85c-.148 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07s-3.584-.012-4.85-.07c-3.252-.148-4.771-1.691-4.919-4.919-.058-1.265-.07-1.645-.07-4.85s.012-3.584.07-4.85C2.25 3.854 3.784 2.31 7.031 2.163 8.297 2.105 8.676 2.093 12 2.093m0-2.093c-3.264 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948s.014 3.667.072 4.947c.2 4.358 2.618 6.78 6.98 6.98 1.281.059 1.689.073 4.948.073s3.667-.014 4.947-.072c4.358-.2 6.78-2.618 6.98-6.98.059-1.281.073-1.689.073-4.948s-.014-3.667-.072-4.947c-.2-4.358-2.618-6.78-6.98-6.98C15.667.014 15.264 0 12 0z"/>
                        <path fill="#fff" d="M12 7.162A4.838 4.838 0 1016.838 12 4.838 4.838 0 0012 7.162zm0 8.004A3.166 3.166 0 1115.166 12 3.166 3.166 0 0112 15.166zM16.949 5.61a1.44 1.44 0 101.44 1.44 1.44 1.44 0 00-1.44-1.44z"/>
                    </svg>
                </a>
                <a href="https://www.tiktok.com/@cncfitnessbsb" target="_blank" rel="noopener noreferrer" class="hover:opacity-80 transition-opacity" aria-label="TikTok">
                    <svg class="h-7 w-7" viewBox="0 0 24 24">
                        <path fill="#010101" d="M12.525.02c1.31-.02 2.61-.01 3.91-.02.08 1.53.63 3.09 1.75 4.17 1.12 1.11 2.7 1.62 4.24 1.79v4.03c-1.44-.05-2.89-.35-4.2-.97-.57-.26-1.1-.59-1.62-.93-.01 2.92.01 5.84-.02 8.75-.08 1.4-.54 2.79-1.35 3.94-1.31 1.92-3.58 3.17-5.91 3.21-1.43.08-2.86-.31-4.08-1.03-2.02-1.19-3.44-3.37-3.65-5.71-.02-.5-.03-1-.01-1.49.18-1.9 1.12-3.72 2.58-4.96 1.66-1.44 3.98-2.13 6.15-1.72.02 1.48-.04 2.96-.04 4.44-.99-.32-2.15-.23-3.02.37-.63.41-1.11 1.04-1.36 1.75-.21.51-.15 1.07-.14 1.61.24 1.64 1.82 3.02 3.5 2.87 1.12-.01 2.19-.66 2.77-1.61.19-.33.4-.67.41-1.06.1-1.79.06-3.57.07-5.36.01-4.03-.01-8.05.02-12.07z"/>
                        <path fill="#fff" d="M12.275,12.07c-.01,4.02,.01,8.04-.02,12.07-.01-1.79-.05-3.57-.07-5.36-.01-.39-.22-.73-.41-1.06-.58-.95-1.65-1.6-2.77-1.61-1.68-.15-3.26,1.23-3.5,2.87,0,.54-.07,1.1,.14,1.61,.25,.71,.73,1.34,1.36,1.75,.87,.6,2.03,.69,3.02,.37v-4.44Z"/>
                        <path fill="#ff0050" d="M12.275,0c.01,4.02,.03,8.04,.02,12.07v-4.44c-2.17-.41-4.49,.28-6.15,1.72-1.46,1.24-2.4,3.06-2.58,4.96.02,.49,.01,.99,.01,1.49,.21,2.34,1.63,4.52,3.65,5.71,1.22,.72,2.65,1.11,4.08,1.03,2.33-.04,4.6-1.29,5.91-3.21,.81-1.15,1.27-2.54,1.35-3.94,.03-2.91-.01-5.83,.02-8.75,.52,.34,1.05,.67,1.62,.93,1.31,.62,2.76,.92,4.2,.97V5.99c-1.54-.17-3.12-.68-4.24-1.79-1.12-1.08-1.67-2.64-1.75-4.17Z"/>
                    </svg>
                </a>
                <a href="https://www.youtube.com/results?search_query=cncfitnessbsb" target="_blank" rel="noopener noreferrer" class="hover:opacity-80 transition-opacity" aria-label="YouTube">
                    <svg class="h-7 w-7" viewBox="0 0 24 24">
                        <path fill="#FF0000" d="M19.615 3.184c-3.604-.246-11.631-.245-15.23 0-3.897.266-4.356 2.62-4.385 8.816.029 6.185.484 8.549 4.385 8.816 3.6.245 11.626.246 15.23 0 3.897-.266 4.356-2.62 4.385-8.816-.029-6.185-.484-8.549-4.385-8.816z"/>
                        <path fill="#FFFFFF" d="M9 15.885V8.115l6.063 3.785L9 15.885z"/>
                    </svg>
                </a>
            </div>
        </div>
    </footer>

    <!-- Mobile CTA Bar -->
    <div class="lg:hidden fixed bottom-0 left-0 right-0 bg-gray-900/80 backdrop-blur-sm p-3 border-t border-gray-700 z-40" style="transform: translateZ(0);">
        <a href="#membership" class="w-full block text-center bg-blue-600 text-white font-semibold px-6 py-3 rounded-lg hover:bg-blue-700 transition-all duration-300" data-lang-key="joinNow">
            Gabung Sekarang
        </a>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            // --- LANGUAGE & CONTENT DATA ---
            const langData = {
                id: {
                    navWhyUs: "Keunggulan", navTrainers: "Pelatih", navTestimonials: "Testimoni", navGallery: "Galeri", navSchedule: "Jadwal", navReels: "Reels", navMembership: "Membership", navLocation: "Lokasi", navContact: "Kontak",
                    joinNow: "Gabung Sekarang",
                    heroTitle: "Capai Target <span class='text-gradient'>Kebugaran</span> Anda",
                    heroSubtitle: "CNC Fitness BSB menyediakan fasilitas premium, pelatih ahli, dan komunitas yang mendukung untuk membantu Anda meraih hasil nyata.",
                    heroCTA: "Lihat Paket Membership",
                    whyUsTitle: "Kenapa Berlatih di CNC Fitness?", whyUsSubtitle: "Kami menyediakan semua yang Anda butuhkan untuk mendukung perjalanan kebugaran Anda.",
                    feature1Title: "Peralatan Terbaik", feature1Desc: "Akses ke peralatan fitness modern untuk latihan yang lebih efektif dan terukur.",
                    feature2Title: "Pelatih Profesional", feature2Desc: "Dapatkan panduan dari tim pelatih bersertifikasi untuk program latihan yang aman dan personal.",
                    feature3Title: "Kelas Beragam", feature3Desc: "Jaga motivasi Anda dengan berbagai pilihan kelas, dari Yoga hingga HIIT yang intens.",
                    feature4Title: "Fasilitas Premium", feature4Desc: "Nikmati lingkungan eksklusif, dilengkapi sauna, lounge, dan ruang ganti yang nyaman.",
                    trainersTitle: "Temui Tim Pelatih Profesional Kami", trainersSubtitle: "Berlatih lebih cerdas dengan bimbingan dari para ahli kebugaran.",
                    trainer1Name: "Andi Setiawan", trainer1Spec: "Kekuatan & Kondisi", trainer1Desc: "Ahli merancang program kekuatan untuk meningkatkan performa dan membentuk postur ideal.",
                    trainer2Name: "Citra Amelia", trainer2Spec: "Penurunan Berat Badan & Nutrisi", trainer2Desc: "Memadukan latihan efektif dengan panduan nutrisi untuk membantu Anda mencapai berat badan ideal.",
                    trainer3Name: "David Lee", trainer3Spec: "Fungsional & Mobilitas", trainer3Desc: "Spesialis latihan fungsional untuk meningkatkan mobilitas dan kekuatan untuk aktivitas sehari-hari.",
                    trainer4Name: "Sari Wulandari", trainer4Spec: "Yoga & Fleksibilitas", trainer4Desc: "Membantu Anda menemukan ketenangan dan meningkatkan kelenturan tubuh melalui yoga.",
                    testimonialsTitle: "Kata Mereka Tentang Kami", testimonialsSubtitle: "Kisah sukses nyata dari para member kami yang luar biasa.",
                    testi1Name: "Ahmad Prasetyo", testi1Date: "25 Juli 2025", testi1Quote: "\"Fasilitasnya luar biasa dan para pelatihnya sangat profesional. Saya berhasil mencapai target berat badan saya dalam 3 bulan. Sangat direkomendasikan!\"",
                    testi2Name: "Siti Nurhaliza", testi2Date: "18 Juni 2025", testi2Quote: "\"Kelas Yoga di sini adalah yang terbaik di Balikpapan. Instrukturnya sabar dan lingkungannya sangat mendukung. Saya merasa lebih bugar dan tenang.\"",
                    testi3Name: "Budi Santoso", testi3Date: "10 Mei 2025", testi3Quote: "\"Komunitas di CNC Fitness sangat positif. Saya tidak hanya mendapatkan tubuh yang lebih sehat, tetapi juga teman-teman baru yang memiliki semangat yang sama.\"",
                    galleryTitle: "Galeri CNC Fitness", gallerySubtitle: "Lihat lebih dekat suasana dan fasilitas kami.",
                    equipmentTitle: "Galeri Peralatan", equipmentSubtitle: "Peralatan modern dan lengkap untuk setiap kebutuhan latihan Anda.",
                    reelsTitle: "Aksi Nyata, Hasil Nyata", reelsSubtitle: "Lihat energi dan komunitas kami melalui Reels terbaru di Instagram.",
                    reelsCTA: "Lihat Semua Reels",
                    scheduleTitle: "Jadwal Kelas Interaktif", scheduleSubtitle: "Filter berdasarkan hari atau tipe kelas untuk menemukan sesi yang sempurna untuk Anda.",
                    filterAll: "Semua", filterMonday: "Senin", filterTuesday: "Selasa", filterWednesday: "Rabu", filterThursday: "Kamis", filterFriday: "Jumat",
                    filterYoga: "Yoga", filterHiit: "HIIT", filterStrength: "Strength",
                    classRegister: "Daftar via WA", instructorLabel: "Instruktur",
                    membershipTitle: "Investasi Untuk Diri Anda", membershipSubtitle: "Pilih paket yang paling sesuai dengan gaya hidup dan tujuan Anda. Komitmen kami adalah transparansi penuh.",
                    plan1Title: "1 Bulan", plan1Subtitle: "Fleksibel & Cepat", plan1Price: "Rp 550.000",
                    planFeatureAllAccess: "Akses semua alat", planFeatureClassAccess: "Akses semua kelas", planFeatureTowel: "Handuk & Loker",
                    planCTA: "Pilih Paket",
                    planPopular: "Paling Populer", plan2Title: "6 Bulan", plan2Subtitle: "Komitmen & Hasil", plan2Price: "Rp 2.750.000", plan2Save: "Hemat Rp 550.000", 
                    plan2Feature1: "Semua di paket 1 Bulan", plan2Feature2: "1x Sesi Personal Trainer", plan2Feature3: "Analisa Komposisi Tubuh",
                    plan3Title: "12 Bulan", plan3Subtitle: "Transformasi Total", plan3Price: "Rp 4.950.000", plan3Save: "Hemat Rp 1.650.000", 
                    plan3Feature1: "Semua di paket 6 Bulan", plan3Feature2: "Merchandise Eksklusif", plan3Feature3: "Konsultasi Nutrisi",
                    trialTitle: "Siap Memulai Perjalanan Anda?", trialSubtitle: "Dapatkan <span class='font-bold'>Free Trial 1 Hari</span> untuk merasakan sendiri pengalaman premium di CNC Fitness. Klaim sekarang!", trialCTA: "Klaim Free Trial via WhatsApp",
                    locationTitle: "Pusat Kebugaran Premium di Balikpapan", locationSubtitle: "Lokasi kami yang strategis di Balikpapan Superblock memudahkan Anda untuk berolahraga kapan saja.",
                    locationAddress: "Balikpapan Superblock, Pentacity Shopping Venue, Lt. 2<br>Jl. Jenderal Sudirman No. 47, Balikpapan, Kalimantan Timur",
                    locationWhatsapp: "0821-9156-2827",
                    locationHours: "Senin - Sabtu: 06:00 - 22:00 | Minggu: 08:00 - 20:00",
                    footerRights: "© 2025 CNC Fitness BSB. Hak Cipta Dilindungi.",
                    waMsgPlan1: "Halo CNC Fitness, saya tertarik dengan paket membership 1 Bulan.",
                    waMsgPlan2: "Halo CNC Fitness, saya tertarik dengan paket membership 6 Bulan.",
                    waMsgPlan3: "Halo CNC Fitness, saya tertarik dengan paket membership 12 Bulan.",
                    waMsgTrial: "Halo CNC Fitness, saya tertarik untuk klaim Free Trial 1 Hari.",
                },
                en: {
                    navWhyUs: "Why Us", navTrainers: "Trainers", navTestimonials: "Testimonials", navGallery: "Gallery", navSchedule: "Schedule", navReels: "Reels", navMembership: "Membership", navLocation: "Location", navContact: "Contact",
                    joinNow: "Join Now",
                    heroTitle: "Achieve Your <span class='text-gradient'>Fitness</span> Goals",
                    heroSubtitle: "CNC Fitness BSB provides premium facilities, expert trainers, and a supportive community to help you achieve real results.",
                    heroCTA: "View Membership Plans",
                    whyUsTitle: "Why Train at CNC Fitness?", whyUsSubtitle: "We provide everything you need to support your fitness journey.",
                    feature1Title: "Best Equipment", feature1Desc: "Access to modern fitness equipment for a more effective and measurable workout.",
                    feature2Title: "Professional Trainers", feature2Desc: "Get guidance from a team of certified trainers for a safe and personalized training program.",
                    feature3Title: "Diverse Classes", feature3Desc: "Stay motivated with a wide range of classes, from calming Yoga to intense HIIT.",
                    feature4Title: "Premium Facilities", feature4Desc: "Enjoy an exclusive environment, complete with a sauna, lounge, and comfortable changing rooms.",
                    trainersTitle: "Meet Our Professional Trainers", trainersSubtitle: "Train smarter with guidance from fitness experts.",
                    trainer1Name: "Andi Setiawan", trainer1Spec: "Strength & Conditioning", trainer1Desc: "Expert in designing strength programs to improve performance and build ideal posture.",
                    trainer2Name: "Citra Amelia", trainer2Spec: "Weight Loss & Nutrition", trainer2Desc: "Combines effective exercises with practical nutrition guidance to help you reach your ideal weight.",
                    trainer3Name: "David Lee", trainer3Spec: "Functional & Mobility", trainer3Desc: "Functional training specialist to improve mobility and strength for daily activities.",
                    trainer4Name: "Sari Wulandari", trainer4Spec: "Yoga & Flexibility", trainer4Desc: "Helps you find calmness and improve body flexibility through yoga.",
                    testimonialsTitle: "What Our Members Say", testimonialsSubtitle: "Real success stories from our amazing members.",
                    testi1Name: "Ahmad Prasetyo", testi1Date: "July 25, 2025", testi1Quote: "\"The facilities are outstanding and the trainers are highly professional. I managed to hit my weight goal in 3 months. Highly recommended!\"",
                    testi2Name: "Siti Nurhaliza", testi2Date: "June 18, 2025", testi2Quote: "\"The Yoga classes here are the best in Balikpapan. The instructors are patient and the environment is very supportive. I feel fitter and calmer.\"",
                    testi3Name: "Budi Santoso", testi3Date: "May 10, 2025", testi3Quote: "\"The community at CNC Fitness is so positive. I've not only gotten a healthier body but also new friends who share the same passion.\"",
                    galleryTitle: "CNC Fitness Gallery", gallerySubtitle: "Take a closer look at our atmosphere and facilities.",
                    equipmentTitle: "Equipment Gallery", equipmentSubtitle: "Modern and complete equipment for your every training need.",
                    reelsTitle: "Real Action, Real Results", reelsSubtitle: "See our energy and community through the latest Reels on Instagram.",
                    reelsCTA: "View All Reels",
                    scheduleTitle: "Interactive Class Schedule", scheduleSubtitle: "Filter by day or class type to find the perfect session for you.",
                    filterAll: "All", filterMonday: "Monday", filterTuesday: "Tuesday", filterWednesday: "Wednesday", filterThursday: "Thursday", filterFriday: "Friday",
                    filterYoga: "Yoga", filterHiit: "HIIT", filterStrength: "Strength",
                    classRegister: "Register via WA", instructorLabel: "Instructor",
                    membershipTitle: "Invest In Yourself", membershipSubtitle: "Choose the plan that best suits your lifestyle and goals. Our commitment is full transparency.",
                    plan1Title: "1 Month", plan1Subtitle: "Flexible & Fast", plan1Price: "IDR 550,000",
                    planFeatureAllAccess: "All equipment access", planFeatureClassAccess: "All classes access", planFeatureTowel: "Towel & Locker",
                    planCTA: "Choose Plan",
                    planPopular: "Most Popular", plan2Title: "6 Months", plan2Subtitle: "Commitment & Results", plan2Price: "IDR 2,750,000", plan2Save: "Save IDR 550,000", 
                    plan2Feature1: "All in 1 Month plan", plan2Feature2: "1x Personal Trainer Session", plan2Feature3: "Body Composition Analysis",
                    plan3Title: "12 Months", plan3Subtitle: "Total Transformation", plan3Price: "IDR 4,950,000", plan3Save: "Save IDR 1,650,000", 
                    plan3Feature1: "All in 6 Months plan", plan3Feature2: "Exclusive Merchandise", plan3Feature3: "Nutrition Consultation",
                    trialTitle: "Ready to Start Your Journey?", trialSubtitle: "Get a <span class='font-bold'>1-Day Free Trial</span> to experience the premium feel of CNC Fitness yourself. Claim it now!", trialCTA: "Claim Free Trial via WhatsApp",
                    locationTitle: "Premium Fitness Center in Balikpapan", locationSubtitle: "Our strategic location at Balikpapan Superblock makes it easy for you to work out anytime.",
                    locationAddress: "Balikpapan Superblock, Pentacity Shopping Venue, 2nd Floor<br>Jl. Jenderal Sudirman No. 47, Balikpapan, East Kalimantan",
                    locationWhatsapp: "0821-9156-2827",
                    locationHours: "Mon - Sat: 06:00 AM - 10:00 PM | Sun: 08:00 AM - 08:00 PM",
                    footerRights: "© 2025 CNC Fitness BSB. All Rights Reserved.",
                    waMsgPlan1: "Hello CNC Fitness, I'm interested in the 1 Month membership plan.",
                    waMsgPlan2: "Hello CNC Fitness, I'm interested in the 6 Months membership plan.",
                    waMsgPlan3: "Hello CNC Fitness, I'm interested in the 12 Months membership plan.",
                    waMsgTrial: "Hello CNC Fitness, I'm interested in claiming the 1-Day Free Trial.",
                }
            };
            
            const langIdBtn = document.getElementById('lang-id');
            const langEnBtn = document.getElementById('lang-en');
            const phoneNumber = '6282191562827';

            function changeLanguage(lang) {
                // Set language attribute for the whole document
                document.documentElement.lang = lang;
                
                // Update all text elements with data-lang-key
                document.querySelectorAll('[data-lang-key]').forEach(el => {
                    const key = el.dataset.langKey;
                    if (langData[lang][key]) {
                        el.innerHTML = langData[lang][key];
                    }
                });
                
                // Update active state for language switcher flags
                if (lang === 'id') {
                    langIdBtn.classList.add('active');
                    langEnBtn.classList.remove('active');
                } else {
                    langEnBtn.classList.add('active');
                    langIdBtn.classList.remove('active');
                }
                
                // Update all WhatsApp links with the correct message for the selected language
                document.querySelectorAll('a[data-wa-key]').forEach(link => {
                    const key = link.dataset.waKey;
                    let messageKey;
                    switch(key) {
                        case 'plan1': messageKey = 'waMsgPlan1'; break;
                        case 'plan2': messageKey = 'waMsgPlan2'; break;
                        case 'plan3': messageKey = 'waMsgPlan3'; break;
                        case 'trial': messageKey = 'waMsgTrial'; break;
                    }
                    if (messageKey && langData[lang][messageKey]) {
                        const message = encodeURIComponent(langData[lang][messageKey]);
                        link.href = `https://api.whatsapp.com/send?phone=${phoneNumber}&text=${message}`;
                    }
                });
                
                // Re-render the schedule with the new language
                const activeFilter = document.querySelector('#schedule-filters .filter-btn.active');
                if (activeFilter) {
                    renderSchedule(activeFilter.dataset.filter, lang);
                }
            }

            langIdBtn.addEventListener('click', () => changeLanguage('id'));
            langEnBtn.addEventListener('click', () => changeLanguage('en'));
            
            // --- DYNAMIC EFFECTS SCRIPTS ---
            const heroSection = document.getElementById('home');
            heroSection.addEventListener('mousemove', e => {
                const rect = heroSection.getBoundingClientRect();
                heroSection.style.setProperty('--x', `${e.clientX - rect.left}px`);
                heroSection.style.setProperty('--y', `${e.clientY - rect.top}px`);
            });

            const cards = document.querySelectorAll('.card-3d');
            cards.forEach(card => {
                card.addEventListener('mousemove', e => {
                    const rect = card.getBoundingClientRect();
                    const { width, height, left, top } = rect;
                    const x = e.clientX - left;
                    const y = e.clientY - top;
                    const rotateX = (y / height - 0.5) * -15;
                    const rotateY = (x / width - 0.5) * 15;
                    card.style.setProperty('--rotate-x', `${rotateX}deg`);
                    card.style.setProperty('--rotate-y', `${rotateY}deg`);
                });
                card.addEventListener('mouseleave', () => {
                    card.style.setProperty('--rotate-x', '0deg');
                    card.style.setProperty('--rotate-y', '0deg');
                });
            });

            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('is-visible');
                    }
                });
            }, { threshold: 0.1 });

            document.querySelectorAll('.scroll-animate').forEach(el => observer.observe(el));

            // --- UI SCRIPTS ---
            const mobileMenuButton = document.getElementById('mobile-menu-button');
            const mobileMenu = document.getElementById('mobile-menu');
            const mobileLinks = document.querySelectorAll('.mobile-link');

            mobileMenuButton.addEventListener('click', () => mobileMenu.classList.toggle('hidden'));
            mobileLinks.forEach(link => {
                link.addEventListener('click', () => {
                    if (!mobileMenu.classList.contains('hidden')) {
                        mobileMenu.classList.add('hidden');
                    }
                });
            });

            // FIX: Use a more specific selector to avoid targeting javascript/external links.
            document.querySelectorAll('a[href^="#"]:not([href="#"])').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    const targetElement = document.querySelector(this.getAttribute('href'));
                    if (targetElement) {
                        const headerOffset = document.getElementById('header').offsetHeight;
                        const elementPosition = targetElement.getBoundingClientRect().top;
                        const offsetPosition = elementPosition + window.pageYOffset - headerOffset;

                        window.scrollTo({
                            top: offsetPosition,
                            behavior: "smooth"
                        });
                    }
                });
            });

            const header = document.getElementById('header');
            window.addEventListener('scroll', () => {
                header.classList.toggle('bg-black/80', window.scrollY > 50);
                header.classList.toggle('bg-black/30', window.scrollY <= 50);
            });
            
            // --- SCHEDULE SCRIPT ---
            const scheduleData = [
                { day: 'senin', time: '07:00', name: 'Morning Flow Yoga', type: 'yoga', instructor: 'Amanda' },
                { day: 'senin', time: '18:00', name: 'Full Body Strength', type: 'strength', instructor: 'David' },
                { day: 'selasa', time: '08:00', name: 'Ignite HIIT', type: 'hiit', instructor: 'Sarah' },
                { day: 'selasa', time: '19:00', name: 'Power Yoga', type: 'yoga', instructor: 'Amanda' },
                { day: 'rabu', time: '07:00', name: 'Core & Glutes', type: 'strength', instructor: 'David' },
                { day: 'rabu', time: '18:00', name: 'Vinyasa Yoga', type: 'yoga', instructor: 'Sari' },
                { day: 'rabu', time: '19:00', name: 'Metabolic HIIT', type: 'hiit', instructor: 'Sarah' },
                { day: 'kamis', time: '08:00', name: 'Upper Body Blast', type: 'strength', instructor: 'David' },
                { day: 'kamis', time: '19:00', name: 'Endurance HIIT', type: 'hiit', instructor: 'Andi' },
                { day: 'jumat', time: '07:00', name: 'Restorative Yoga', type: 'yoga', instructor: 'Amanda' },
                { day: 'jumat', time: '17:00', name: 'Weekend Warrior HIIT', type: 'hiit', instructor: 'Sarah' },
                { day: 'jumat', time: '18:00', name: 'Foundation Strength', type: 'strength', instructor: 'Andi' },
            ];

            const scheduleGrid = document.getElementById('schedule-grid');
            const filterButtons = document.querySelectorAll('#schedule-filters .filter-btn');

            function renderSchedule(filter = 'all', lang = 'id') {
                scheduleGrid.innerHTML = '';
                const filteredData = scheduleData.filter(item => {
                    if (filter === 'all') return true;
                    return item.day === filter || item.type === filter;
                });

                if (filteredData.length === 0) {
                    const noClassText = lang === 'id' ? 'Tidak ada kelas yang tersedia untuk filter ini.' : 'No classes available for this filter.';
                    scheduleGrid.innerHTML = `<p class="text-gray-400 text-center col-span-full">${noClassText}</p>`;
                    return;
                }

                filteredData.forEach(item => {
                    const dayKey = `filter${item.day.charAt(0).toUpperCase() + item.day.slice(1)}`;
                    const dayName = langData[lang][dayKey] || item.day;
                    
                    const registerText = langData[lang].classRegister;
                    const instructorLabel = langData[lang].instructorLabel;
                    const waTextId = `Halo CNC Fitness, saya tertarik untuk mendaftar kelas ${item.name} pada hari ${dayName} jam ${item.time}.`;
                    const waTextEn = `Hello CNC Fitness, I'm interested in registering for the ${item.name} class on ${dayName} at ${item.time}.`;
                    const waMessage = lang === 'id' ? encodeURIComponent(waTextId) : encodeURIComponent(waTextEn);
                    const waLink = `https://api.whatsapp.com/send?phone=${phoneNumber}&text=${waMessage}`;

                    const div = document.createElement('div');
                    div.className = 'schedule-item flex flex-col justify-between p-6 rounded-xl gradient-border';
                    div.innerHTML = `
                        <div>
                            <div class="flex justify-between items-start mb-4">
                                <div>
                                    <p class="text-xs uppercase tracking-widest text-blue-400 font-semibold">${dayName}</p>
                                    <h4 class="text-xl font-bold text-white mt-1">${item.name}</h4>
                                </div>
                                <p class="text-xl font-bold text-white flex-shrink-0">${item.time}</p>
                            </div>
                            <div class="flex justify-between items-center text-sm">
                                <p class="text-gray-400">${instructorLabel}: ${item.instructor}</p>
                                <span class="text-xs font-bold uppercase py-1 px-3 rounded-full bg-gray-700 text-gray-200">${item.type}</span>
                            </div>
                        </div>
                        <a href="${waLink}" target="_blank" rel="noopener noreferrer" class="mt-6 block w-full text-center bg-blue-600 text-white font-semibold py-2.5 rounded-lg hover:bg-blue-500 transition-colors">
                            ${registerText}
                        </a>
                    `;
                    scheduleGrid.appendChild(div);
                });
            }

            filterButtons.forEach(button => {
                button.addEventListener('click', () => {
                    filterButtons.forEach(btn => {
                        btn.classList.remove('active', 'bg-blue-600', 'text-white');
                        btn.classList.add('border-gray-600', 'text-gray-300', 'hover:bg-gray-700');
                    });
                    button.classList.add('active', 'bg-blue-600', 'text-white');
                    button.classList.remove('border-gray-600', 'text-gray-300', 'hover:bg-gray-700');
                    const currentLang = document.documentElement.lang;
                    renderSchedule(button.dataset.filter, currentLang);
                });
            });

            // Initial render on page load
            changeLanguage('id');
        });
    </script>
</body>
</html>
