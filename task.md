Task Execution List

Instruksi: Ikuti urutan task secara linier. Jangan eksekusi task berikutnya sebelum task saat ini selesai dan diverifikasi.
Phase 1: Environment Setup

     1.1 Buat file kosong bernama index.html di root folder proyek.
     1.2 Ketikkan struktur dasar HTML5 (<!DOCTYPE html>, <html>, <head>, <body>).
     1.3 Tambahkan tag <script src="https://cdn.tailwindcss.com"></script> di dalam <head>.
     1.4 Tambahkan tag <link> Google Fonts untuk font 'Inter' (weights: 400, 500, 600, 700).
     1.5 Inject konfigurasi Tailwind (tailwind.config = { ... }) di dalam tag <script> baru di bawah CDN untuk warna (ax-gray, ax-dark, ax-orange) dan Font (sans: ['Inter']).
     1.6 Tambahkan blok <style> untuk custom CSS class: .animate-gradient (keyframes moveGradient) dan .text-roll-container / .text-roll-inner (overflow hidden, translateY manipulation).

Phase 2: Layout & Content Implementation

     2.1 [NAVBAR]: Buat container pembungkus dengan flex justify-center pt-4. Di dalamnya, buat pill bg-white rounded-full p-1.5 flex items-center justify-between.
     2.2 [NAVBAR]: Implementasi Logo hitam (flex, circle, teks "MI") dan Link navigasi (hidden di mobile, flex di md+).
     2.3 [NAVBAR]: Implementasi area kanan: Span kosong untuk Jam dengan ID id="live-clock", dan tombol hitam CTA dengan struktur text-roll (2 span teks di dalam container h-5 overflow-hidden) dan ikon panah lingkaran putih.
     2.4 [HERO]: Buat <section> dengan relative h-screen flex flex-col overflow-hidden.
     2.5 [HERO]: Tambahkan div latar belakang gradien dengan posisi absolute inset-0 dan class .animate-gradient.
     2.6 [HERO]: Buat kontainer konten z-10, flex flex-col justify-end. Masukkan label kecil, <h1> dengan fluid typography dan pemisah <br> responsif, serta row CTA (Tombol Oranye text-roll + Badge Partner).
     2.7 [TENTANG]: Buat <section id="tentang"> dengan bg-white pt-16 pb-12 sm:.... 
     2.8 [TENTANG]: Buat baris Badge (Lingkaran hitam "1" + Kapsul border "Tentang Program").
     2.9 [TENTANG]: Buat Heading <h2>.
     2.10 [TENTANG]: Buat grid container. Di dalamnya, buat 2 div layout: Satu untuk Mobile (lg:hidden flex-col), satu untuk Desktop (hidden lg:grid grid-cols-[26%_1fr_48%]). Isi masing-masing dengan gambar Unsplash, teks paragraf, dan tombol CTA sesuai spesifikasi grid.
     2.11 [CTA]: Buat <section id="aksi"> dengan bg-[#F5F5F5].
     2.12 [CTA]: Buat baris Badge (Lingkaran hitam "2" + Kapsul "Aksi Nyata") dan Heading <h2>.
     2.13 [CTA]: Buat Grid 2 kolom (md:grid-cols-2). Isi dengan 2 komponen Kartu.
     2.14 [CTA CARDS]: Buat kartu dengan container gambar (aspect ratio berbeda). Di dalamnya, tambahkan gambar + tombol expand melayang (absolute bottom-4 left-4). Tombol harus berisi ikon dan teks tersembunyi (opacity-0) yang melebar saat kartu di-hover (group-hover:w-[148px]).

Phase 3: Logic Implementation

     3.1 Buat tag <script> sebelum penutup </body>.
     3.2 Tulis fungsi updateClock() yang mengambil new Date(), format ke timezone Asia/Jakarta (HH:MM), dan inject ke innerText elemen #live-clock.
     3.3 Panggil setInterval(updateClock, 1000) dan updateClock() sekali untuk inisialisasi awal.

Phase 4: Quality Assurance (QA) & Visual Audit

     4.1 Buka index.html di Browser. Klik Kanan -> Inspect Element.
     4.2 [RESIZE TEST]: Tarik handle viewport dari 320px hingga 1440px. Pastikan tidak ada teks yang tumpang tindih atau gambar yang aneh.
     4.3 [INTERACTION TEST]: Hover tombol Hitam di Navbar, tombol Oranye di Hero, dan kartu di CTA. Pastikan animasi text-roll bergesar tepat 50% ke atas, ikon panah berputar, dan expanding button membuka lebar tanpa patah-patah.
     4.4 [CODE CLEANUP]: Pastikan tidak ada class Tailwind yang salah ketik, tidak ada tag HTML yang tidak tertutup, dan indentasi rapi.
     4.5 [CODE REVIEW]: Baca ulang kode Anda dan pastikan tidak ada bug yang tersembunyi.
     4.6 Berikan command catatan dokumentasi pada fitur atau component tertentu
