# kehidupan-muji-peter
halaman mengabadikan perjalanan hidup, perjalanan, serta kebersamaan bapak muji dan anaknya peter
```html
<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- Pengaturan SEO Utama agar siap diindeks Google dengan kata kunci "Kehidupan Muji dan Peter" -->
    <title>Kehidupan Muji dan Peter — Kisah Hangat Ayah dan Anak</title>
    <meta name="description" content="Kehidupan Muji dan Peter: Kisah inspiratif tentang perjuangan tulus Bapak Muji dan keseharian anaknya, Peter, dalam menempuh pendidikan dan meraih masa depan cerah.">
    <meta name="keywords" content="Kehidupan Muji dan Peter, Kisah Bapak Muji dan Peter, Biografi Muji dan Peter, Cerita Ayah dan Anak">
    <meta name="author" content="Keluarga Muji & Peter">
    
    <!-- Open Graph untuk tampilan bagikan tautan (WhatsApp, Facebook, dll) -->
    <meta property="og:title" content="Kehidupan Muji dan Peter">
    <meta property="og:description" content="Kisah hangat dan inspiratif tentang perjuangan Bapak Muji dan keseharian sang anak, Peter.">
    <meta property="og:type" content="article">

    <!-- Structured Data (JSON-LD) agar Google lebih mudah memahami halaman artikel biografi ini -->
    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "Article",
      "headline": "Kehidupan Muji dan Peter",
      "description": "Kisah inspiratif dan keseharian Bapak Muji serta anaknya, Peter, dalam menempuh pendidikan dan meraih cita-cita.",
      "author": {
        "@type": "Person",
        "name": "Muji dan Peter"
      }
    }
    </script>

    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts: Inter & Lora untuk kesan artikel editorial yang hangat -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Lora:ital,wght@0,500;0,600;0,700;1,400&display=swap" rel="stylesheet">

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        serif: ['Lora', 'serif'],
                    },
                    colors: {
                        warm: {
                            50: '#FDFBF7',
                            100: '#F7F2E9',
                            200: '#EFE5D3',
                            600: '#B45309',
                            700: '#92400E',
                            800: '#78350F',
                            900: '#451A03',
                        }
                    }
                }
            }
        }
    </script>
</head>
<body class="bg-warm-50 text-stone-800 antialiased selection:bg-amber-200 selection:text-amber-900">

    <!-- Notifikasi Toast (Pengganti alert) -->
    <div id="toast-container" class="fixed bottom-5 right-5 z-50 flex flex-col gap-2 pointer-events-none"></div>

    <!-- Navigasi Atas -->
    <header class="sticky top-0 z-40 bg-warm-50/90 backdrop-blur-md border-b border-stone-200/80">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 py-3.5 flex items-center justify-between gap-3">
            <a href="#" class="flex items-center gap-2.5 group">
                <span class="w-9 h-9 rounded-xl bg-amber-600 text-white flex items-center justify-center font-serif font-bold text-lg shadow-sm group-hover:bg-amber-700 transition">
                    M&P
                </span>
                <div>
                    <span class="font-serif font-bold text-stone-900 text-base sm:text-lg block leading-none">Muji & Peter</span>
                    <span class="text-[11px] text-stone-500 font-medium">Catatan Perjalanan Hidup</span>
                </div>
            </a>

            <!-- Tombol Mode Edit Cerita -->
            <div class="flex items-center gap-2">
                <button id="toggle-edit-btn" onclick="toggleEditMode()" class="inline-flex items-center gap-2 px-3.5 py-2 rounded-xl text-xs sm:text-sm font-semibold bg-white border border-stone-300 text-stone-700 hover:bg-stone-100 active:scale-95 transition shadow-sm">
                    <svg id="edit-icon" class="w-4 h-4 text-amber-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M11 5H6a2 2 0 00-2 2v11a2 2 0 002 2h11a2 2 0 002-2v-5m-1.414-9.414a2 2 0 112.828 2.828L11.828 15H9v-2.828l8.586-8.586z"></path>
                    </svg>
                    <span id="edit-btn-text">Edit Cerita</span>
                </button>
            </div>
        </div>
    </header>

    <!-- Banner Info Mode Edit (Muncul saat mode edit aktif) -->
    <div id="edit-banner" class="hidden bg-amber-600 text-white px-4 py-2.5 text-center text-xs sm:text-sm font-medium shadow-inner">
        Mode Edit Aktif: Klik langsung pada judul atau paragraf cerita di bawah untuk mengubah teks, lalu klik <strong>Simpan Perubahan</strong>.
    </div>

    <!-- Konten Utama -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 py-8 sm:py-12">

        <!-- 1. Hero Section -->
        <section class="text-center max-w-2xl mx-auto mb-10 sm:mb-14">
            <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-amber-100/80 text-amber-800 text-xs font-semibold mb-4 border border-amber-200/70">
                <span>Biografi Keluarga</span>
                <span>•</span>
                <span>Kisah Inspiratif</span>
            </div>

            <h1 id="hero-title" class="editable-text font-serif text-3xl sm:text-5xl font-bold text-stone-900 tracking-tight leading-tight mb-4 rounded-lg px-2 py-1 transition">
                Kehidupan Muji dan Peter
            </h1>

            <p id="hero-subtitle" class="editable-text text-base sm:text-lg text-stone-600 leading-relaxed rounded-lg px-2 py-1 transition">
                Sebuah catatan sederhana tentang ketulusan langkah seorang ayah bernama Bapak Muji, dan semangat belajar sang buah hati, Peter, dalam merajut mimpi dari bangku sekolah.
            </p>

            <!-- Daftar Isi Cepat -->
            <nav aria-label="Navigasi Bab" class="mt-6 flex flex-wrap items-center justify-center gap-2 text-xs sm:text-sm">
                <a href="#galeri-peter" class="px-3 py-1.5 rounded-lg bg-white border border-stone-200 text-stone-600 hover:border-amber-400 hover:text-amber-700 transition">Potret Peter</a>
                <a href="#bab-1" class="px-3 py-1.5 rounded-lg bg-white border border-stone-200 text-stone-600 hover:border-amber-400 hover:text-amber-700 transition">1. Perjuangan Bapak Muji</a>
                <a href="#bab-2" class="px-3 py-1.5 rounded-lg bg-white border border-stone-200 text-stone-600 hover:border-amber-400 hover:text-amber-700 transition">2. Keseharian Peter</a>
                <a href="#bab-3" class="px-3 py-1.5 rounded-lg bg-white border border-stone-200 text-stone-600 hover:border-amber-400 hover:text-amber-700 transition">3. Harapan Masa Depan</a>
            </nav>
        </section>

        <!-- 2. Bagian Galeri / Foto Utama Peter -->
        <section id="galeri-peter" class="mb-12 sm:mb-16">
            <div class="bg-white rounded-3xl p-4 sm:p-6 shadow-sm border border-stone-200/80">
                <div class="grid grid-cols-1 md:grid-cols-12 gap-6 items-center">
                    
                    <!-- Bingkai Foto -->
                    <div class="md:col-span-6 relative group">
                        <div class="aspect-[3/4] w-full max-w-sm mx-auto rounded-2xl overflow-hidden bg-stone-100 border border-stone-200 shadow-inner relative">
                            <img 
                                id="peter-photo" 
                                src="36495.jpg" 
                                alt="Peter sedang belajar di ruang kelas sekolah" 
                                class="w-full h-full object-cover object-center transition duration-300"
                                onerror="this.onerror=null; this.src='https://placehold.co/600x800/F5EFE6/78350F?text=Foto+Peter+%0A(Klik+Ganti+Foto+di+Samping)';"
                            >
                            <!-- Label sudut foto -->
                            <div class="absolute bottom-3 left-3 right-3 bg-stone-900/75 backdrop-blur-sm text-white px-3.5 py-2 rounded-xl text-xs flex items-center justify-between">
                                <span class="font-medium">Peter — Masa Sekolah</span>
                                <span class="text-amber-300">Dokumentasi Keluarga</span>
                            </div>
                        </div>
                    </div>

                    <!-- Keterangan Foto & Tombol Ganti Foto -->
                    <div class="md:col-span-6 flex flex-col justify-center space-y-4">
                        <div class="inline-flex items-center gap-1.5 text-amber-700 font-semibold text-xs uppercase tracking-wider">
                            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 9a2 2 0 012-2h.93a2 2 0 001.664-.89l.812-1.22A2 2 0 0110.07 4h3.86a2 2 0 011.664.89l.812 1.22A2 2 0 0018.07 7H19a2 2 0 012 2v9a2 2 0 01-2 2H5a2 2 0 01-2-2V9z"></path>
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 13a3 3 0 11-6 0 3 3 0 016 0z"></path>
                            </svg>
                            <span>Potret Kenangan</span>
                        </div>

                        <h2 id="photo-title" class="editable-text font-serif text-2xl sm:text-3xl font-bold text-stone-900 rounded-lg px-1 py-0.5">
                            Semangat Peter di Bangku Kelas
                        </h2>

                        <p id="photo-caption" class="editable-text text-stone-600 text-sm sm:text-base leading-relaxed rounded-lg px-1 py-0.5">
                            Di balik meja kayu kelas dengan buku catatan Bahasa Indonesia yang terbuka, Peter menjalani hari-harinya sebagai pelajar dengan penuh rasa ingin tahu. Setiap lembar catatan yang ditulisnya adalah wujud bakti kecil untuk membalas kerja keras sang ayah, Bapak Muji.
                        </p>

                        <!-- Input File Tersembunyi + Tombol Interaktif -->
                        <div class="pt-2">
                            <input type="file" id="photo-upload-input" accept="image/*" class="hidden" onchange="handlePhotoUpload(event)">
                            
                            <div class="flex flex-wrap items-center gap-3">
                                <button type="button" onclick="document.getElementById('photo-upload-input').click()" class="inline-flex items-center gap-2 px-4 py-3 rounded-xl bg-amber-600 hover:bg-amber-700 text-white font-semibold text-sm shadow-sm active:scale-95 transition cursor-pointer">
                                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-8l-4-4m0 0L8 8m4-4v12"></path>
                                    </svg>
                                    <span>Ganti / Pilih Foto</span>
                                </button>

                                <button type="button" id="reset-photo-btn" onclick="resetPhoto()" class="hidden px-3.5 py-3 rounded-xl bg-stone-100 hover:bg-stone-200 text-stone-700 font-medium text-xs sm:text-sm transition">
                                    Kembalikan Foto Awal
                                </button>
                            </div>
                            <p class="text-xs text-stone-400 mt-2">
                                Pilih foto langsung dari galeri HP atau komputer Anda untuk memperbarui potret di atas.
                            </p>
                        </div>
                    </div>

                </div>
            </div>
        </section>

        <!-- 3. Bab-Bab Cerita Terstruktur -->
        <section class="space-y-8">
            
            <!-- Bab 1 -->
            <article id="bab-1" class="bg-white rounded-3xl p-6 sm:p-8 shadow-sm border border-stone-200/80 transition hover:border-amber-200">
                <div class="flex items-center gap-3 mb-4">
                    <span class="w-10 h-10 rounded-2xl bg-amber-100 text-amber-800 font-serif font-bold flex items-center justify-center text-base shrink-0">
                        01
                    </span>
                    <div>
                        <span class="text-xs font-semibold uppercase tracking-wider text-amber-700 block">Bab Pertama</span>
                        <h2 id="bab1-title" class="editable-text font-serif text-xl sm:text-2xl font-bold text-stone-900 rounded-lg px-1">
                            Awal Perjuangan Bapak Muji
                        </h2>
                    </div>
                </div>
                <div class="space-y-4 text-stone-700 text-sm sm:text-base leading-relaxed">
                    <p id="bab1-p1" class="editable-text rounded-lg p-1">
                        Bagi Bapak Muji, hidup bukanlah tentang seberapa banyak harta yang dimiliki, melainkan seberapa besar tanggung jawab yang mampu dipikul demi keluarga. Sejak pagi buta sebelum matahari terbit sepenuhnya, Bapak Muji sudah bersiap memulai hari dengan langkah mantap dan doa yang tak pernah putus.
                    </p>
                    <p id="bab1-p2" class="editable-text rounded-lg p-1">
                        Setiap tetes keringat yang jatuh dalam kesehariannya memiliki satu tujuan utama: memastikan Peter mendapatkan kehidupan yang layak serta kesempatan belajar yang jauh lebih baik. Kesederhanaan dan ketekunan Bapak Muji menjadi teladan nyata yang diam-diam membentuk karakter kuat dalam diri Peter.
                    </p>
                </div>
            </article>

            <!-- Bab 2 -->
            <article id="bab-2" class="bg-white rounded-3xl p-6 sm:p-8 shadow-sm border border-stone-200/80 transition hover:border-amber-200">
                <div class="flex items-center gap-3 mb-4">
                    <span class="w-10 h-10 rounded-2xl bg-amber-100 text-amber-800 font-serif font-bold flex items-center justify-center text-base shrink-0">
                        02
                    </span>
                    <div>
                        <span class="text-xs font-semibold uppercase tracking-wider text-amber-700 block">Bab Kedua</span>
                        <h2 id="bab2-title" class="editable-text font-serif text-xl sm:text-2xl font-bold text-stone-900 rounded-lg px-1">
                            Keseharian Peter di Sekolah
                        </h2>
                    </div>
                </div>
                <div class="space-y-4 text-stone-700 text-sm sm:text-base leading-relaxed">
                    <p id="bab2-p1" class="editable-text rounded-lg p-1">
                        Mengenakan seragam batik biru kebanggaannya, Peter menjalani hari-hari di bangku sekolah menengah dengan penuh semangat. Di ruang kelas yang sederhana—dengan lukisan pohon hijau di dinding dan buku-buku pelajaran di atas meja—Peter belajar memahami berbagai mata pelajaran, mulai dari Bahasa Indonesia hingga ilmu pengetahuan lainnya.
                    </p>
                    <p id="bab2-p2" class="editable-text rounded-lg p-1">
                        Di sela-sela waktu belajar dan bertukar cerita bersama teman-teman sebangkunya, Peter selalu mengingat pesan Bapak Muji untuk menjaga kejujuran, menghormati guru, serta tidak mudah menyerah saat menghadapi kesulitan dalam belajar.
                    </p>
                </div>
            </article>

            <!-- Bab 3 -->
            <article id="bab-3" class="bg-white rounded-3xl p-6 sm:p-8 shadow-sm border border-stone-200/80 transition hover:border-amber-200">
                <div class="flex items-center gap-3 mb-4">
                    <span class="w-10 h-10 rounded-2xl bg-amber-100 text-amber-800 font-serif font-bold flex items-center justify-center text-base shrink-0">
                        03
                    </span>
                    <div>
                        <span class="text-xs font-semibold uppercase tracking-wider text-amber-700 block">Bab Ketiga</span>
                        <h2 id="bab3-title" class="editable-text font-serif text-xl sm:text-2xl font-bold text-stone-900 rounded-lg px-1">
                            Harapan dan Masa Depan
                        </h2>
                    </div>
                </div>
                <div class="space-y-4 text-stone-700 text-sm sm:text-base leading-relaxed">
                    <p id="bab3-p1" class="editable-text rounded-lg p-1">
                        Perjalanan kehidupan Muji dan Peter adalah cerminan hangat dari ikatan ayah dan anak yang saling menguatkan. Bapak Muji menanam benih kerja keras dan kesabaran, sementara Peter merawatnya melalui semangat belajar dan cita-cita yang tinggi.
                    </p>
                    <p id="bab3-p2" class="editable-text rounded-lg p-1">
                        Ke depan, keduanya melangkah dengan penuh keyakinan bahwa setiap usaha tulus hari ini akan berbuah kebahagiaan di masa mendatang—membawa kebanggaan bukan hanya bagi keluarga kecil mereka, tetapi juga memberi inspirasi bagi siapa saja yang membaca kisah ini.
                    </p>
                </div>

                <!-- Kutipan Penutup -->
                <blockquote class="mt-6 p-5 rounded-2xl bg-warm-100/80 border-l-4 border-amber-600 text-stone-800 italic font-serif text-sm sm:text-base">
                    <p id="quote-text" class="editable-text rounded px-1">
                        "Langkah kecil yang ditempuh bersama dengan ketulusan akan selalu menemukan jalan menuju masa depan yang cerah."
                    </p>
                    <footer class="mt-2 not-italic font-sans text-xs font-semibold text-amber-800">
                        — Kisah Kehidupan Muji dan Peter
                    </footer>
                </blockquote>
            </article>

        </section>

        <!-- Kotak Info Agar Muncul di Pencarian Google & Bagikan -->
        <section class="mt-12 bg-stone-900 text-stone-200 rounded-3xl p-6 sm:p-8 shadow-md">
            <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-6">
                <div class="space-y-2 max-w-xl">
                    <span class="inline-block px-2.5 py-1 rounded-md bg-amber-500/20 text-amber-300 text-xs font-semibold">
                        Siap Dipublikasikan & Diindeks Google
                    </span>
                    <h3 class="font-serif text-xl font-bold text-white">
                        Bagikan Halaman "Kehidupan Muji dan Peter"
                    </h3>
                    <p class="text-xs sm:text-sm text-stone-400 leading-relaxed">
                        Halaman ini sudah dilengkapi struktur judul dan deskripsi SEO <strong>"Kehidupan Muji dan Peter"</strong>. Setelah file HTML ini diunggah ke hosting (seperti GitHub Pages, Netlify, atau Vercel) dan didaftarkan ke Google Search Console, halaman ini akan mudah ditemukan saat dicari di Google.
                    </p>
                </div>

                <div class="flex flex-col sm:flex-row gap-3 shrink-0">
                    <button type="button" onclick="copyPageSummary()" class="px-4 py-3 rounded-xl bg-amber-600 hover:bg-amber-500 text-white font-semibold text-xs sm:text-sm transition active:scale-95 text-center">
                        Salin Ringkasan Cerita
                    </button>
                    <button type="button" onclick="resetAllContent()" class="px-4 py-3 rounded-xl bg-