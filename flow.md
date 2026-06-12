Alur Pengguna & Interaksi (User & Interaction Flow)
1. Core User Flow (Alur Utama Makro)

Alur ini mendefinisikan perjalanan pengguna dari detik pertama membuka halaman hingga mencapai tujuan akhir (Konversi). Halaman ini dirancang dengan model Linear Funnel (tidak ada navigasi yang membingungkan).

Step 1: Awareness & Hook (Hero Section)

     Trigger: Pengguna membuka link URL (Entry Point).
     Action: Browser me-render Hero Section (Full Viewport).
     Response Sistem: Latar belakang gradien beranimasi perlahan menarik perhatian mata. Jam live berdetak di navbar memberikan kesan "hidup".
     State Pengguna: Terpana oleh tipografi raksasa headline "Berkarya melalui kreativitas dan teknologi untuk dampak positif Indonesia." Pengguna memahami konteks halaman ini dalam 3 detik pertama.
     Decision Point: 
         A: Pengguna langsung tertarik dan mengklik tombol Oranye "Gabung Sekarang" (Direct Conversion -> Lompat ke Step 4).
         B: Pengguna butuh sedikit keyakinan, lalu melakukan scroll ke bawah.

Step 2: Consideration & Trust Building (Tentang Program Section)

     Trigger: Pengguna meng-scroll melewati batas bawah viewport Hero.
     Response Sistem: Latar belakang berubah menjadi putih bersih. Mata pengguna dituntun oleh label "1 / Tentang Program" ke heading sub-bab.
     State Pengguna: Membaca narasi dan melihat komposisi visual editorial (gambar + teks). Memahami value proposition program Magang Mahreen Indonesia.
     Decision Point:
         A: Pengguna mengklik tombol "Pelajari Lebih Lanjut" (Anchor link -> Lompat ke Step 3).
         B: Pengguna melanjutkan scroll alami ke bawah.

Step 3: Action & Conversion (Call to Action Section)

     Trigger: Pengguna tiba di Section CTA.
     Response Sistem: Latar bergeser ke abu-abu lembut #F5F5F5. Label berubah menjadi "2 / Aksi Nyata". Pengguna dihadapkan pada pertanyaan langsung: "Siap berkarya?".
     State Pengguna: Melihat 2 kartu visual (Kreativitas & Teknologi). Pengguna merasa dipilih dan diajak untuk memilih jalur aksinya.
     Decision Point: Pengguna mengarahkan kursor (hover) ke salah satu kartu.

Step 4: Exit / Conversion (Formulir Mahreen)

     Trigger: Pengguna mengklik tombol expanding di dalam kartu atau tombol "Daftar Internship" di Navbar.
     Action: Browser membuka tab baru menuju link eksternal Formulir Mahreen Indonesia (https://bit.ly/FormTestPsikotestMahreenIndonesia).
     State Sistem: Tidak ada broken link, halaman formulir berhasil dimuat. Tugas Landing Page selesai.

2. Interaction Flow (Alur Mikro Interaksi UI)

Alur ini mendefinisikan bagaimana komponen UI merespons input pengguna secara real-time. Semua alur ini harus terjadi secara mulus (seamless) untuk mempertahankan kesan premium.
2.1 Navbar - Text Roll & Arrow Flow

    Idle State: Tombol hitam terlihat. Teks "Daftar Internship" baris pertama terlihat jelas. Ikon panah putih di dalam lingkaran berada di posisi miring (-45deg).
    Hover State (Mouse Masuk): 
         Container teks bergeser ke atas (translateY(-50%)), menampilkan teks "Daftar Internship" baris kedua yang identik.
         Lingkaran putih ikon panah berputar perlahan ke posisi horizontal (0deg).
         Transisi berlangsung selama 500ms dengan kurva cubic-bezier(0.25, 0.1, 0.25, 1).
    Mouse Leave: Semua elemen kembali ke Idle State dengan durasi dan easing yang sama.

2.2 CTA Cards - Expanding Button Flow

    Idle State: Kartu statis. Tombol melayang di pojok kiri bawah hanyalah lingkaran kecil (36x36px) berisi ikon. Teks "Gabung Kreativitas" tersembunyi (opacity-0, lebar container tertahan overflow).
    Card Hover State (Mouse Masuk ke area kartu):
         Gambar di dalam kartu melakukan zoom-in perlahan (scale: 1.05, durasi 700ms).
         Lingkaran tombol melebar horizontal secara instan namun halus (berubah dari w-9 ke w-[148px], durasi 300ms).
         Teks di dalam tombol muncul (opacity 0 -> 100) dengan sedikit jeda (delay 100ms) agar tidak menabrak dinding kapsul yang sedang melebar.
         Ikon ranta/panah berputar dari -45deg ke 0deg.
    Card Hover State (Mouse Keluar dari area kartu):
         Teks langsung menghilang (opacity 100 -> 0).
         Tombol menyusut kembali menjadi lingkaran (durasi 300ms).
         Gambar zoom-out kembali ke ukuran semula.

2.3 Live Clock Flow

    Init: Saat DOM sepenuhnya dimuat, JavaScript memanggil fungsi updateClock().
    Render: Fungsi mengambil waktu lokal browser, mengkonversinya ke zona waktu Asia/Jakarta, memformatnya menjadi HH:MM, dan menyuntikkannya ke DOM.
    Loop: Fungsi dijadwalkan ulang setiap 1000ms (1 detik) menggunakan setInterval, meng-overwrite teks jam di navbar tanpa me-refresh halaman.