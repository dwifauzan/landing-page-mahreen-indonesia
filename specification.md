Software Requirements Specification (SRS)
1. Lingkup Produk

Produk adalah sebuah halaman web statis (Single-Page) yang diakses melalui browser, berisi ajakan bagi generasi muda untuk bergabung dengan program Mahreen Indonesia.
2. Tech Stack & Environment

    Core Markup: HTML5 (Semantic: <nav>, <section>, <h1>, <h2>).
    Styling Engine: Tailwind CSS v3.4 via CDN (https://cdn.tailwindcss.com).
    Custom Configuration: Tailwind config disuntikkan via <script> untuk mendefinisikan font sans: ['Inter', 'system-ui'] dan warna kustom (ax-gray: '#EFEFEF', ax-dark: '#111827', ax-orange: '#F26522').
    Font Loading: Google Fonts CDN (Inter: weights 400, 500, 600, 700).
    Client Logic: Vanilla JavaScript (ES6). Tanpa DOM framework.

3. Spesifikasi Fungsional (Functional Requirements)
FR-01: Sistem Navigasi (Floating Pill)

    FR-01.1: Navbar harus memiliki posisi relatif, melayang di atas hero, dengan styling bg-white rounded-full p-1.5 sm:p-2 shadow-sm.
    FR-01.2: Sistem harus menampilkan jam real-time (WIB) yang diperbarui setiap 1 detik menggunakan setInterval dan toLocaleTimeString('id-ID', { timeZone: 'Asia/Jakarta' }).
    FR-01.3: Tombol CTA "Daftar Internship" harus memicu animasi Text Roll saat di-hover.

FR-02: Hero Section

    FR-02.1: Background harus memutar animasi gradien CSS tanpa henti (loop) dengan durasi 15 detik.
    FR-02.2: Konten hero harus menempel di bagian bawah viewport (flex flex-col justify-end), bukan di tengah.
    FR-02.3: Headline harus menggunakan fluid typography clamp(1.75rem, 7vw, 4.2rem) untuk mobile dan clamp(2.5rem, 5vw, 4.2rem) untuk SM ke atas.

FR-03: Tentang Program Section

    FR-03.1: Pada viewport Desktop (lg+), layout harus menggunakan grid asimetris grid-cols-[26%_1fr_48%].
    FR-03.2: Kolom pertama (26%) dan ketiga (48%) menampilkan aset gambar dengan self-end (melekat ke bawah). Kolom kedua (1fr) menampilkan teks dengan self-start dan justify-end untuk menciptakan ruang negatif dinamis.
    FR-03.3: Pada viewport Mobile/Tablet (lg down), layout harus beralih menjadi Flex Column standar.

FR-04: Call to Action Section

    FR-04.1: Menampilkan 2 kartu dalam grid 2-kolom (1-kolom di mobile).
    FR-04.2: Setiap kartu harus memiliki Expanding Button (lingkaran 36x36px yang melebar menjadi kapsul ~148px/168px saat kartu di-hover, menggunakan transition-all duration-300 ease-in-out).
    FR-04.3: Teks di dalam expanding button harus memiliki opacity 0 dan muncul opacity 100 dengan delay-100 saat hover.

4. Spesifikasi Non-Fungsional (Non-Functional Requirements)
NFR-01: Performa

    Tidak boleh ada render-blocking JavaScript selain inisialisasi Tailwind.
    Total ukuran file HTML tidak boleh melebihi 50KB (tanpa aset gambar eksternal).
    Animasi CSS harus menggunakan properti transform dan opacity untuk memastikan rendering di GPU kompositor (hindari layout thrashing).

NFR-02: Responsivitas

    Breakpoint Wajib: 640px (sm), 768px (md), 1024px (lg), 1280px (xl).
    Tidak boleh ada teks yang overflow atau gambar yang stretch pada lebar 320px hingga 1920px.

NFR-03: Aksesibilitas (A11y)

    Hirarki heading harus ketat: Satu <h1> di Hero, <h2> di section berikutnya.
    Ikon dekoratif harus memiliki atribut aria-hidden="true" jika tidak membawa makna fungsional, atau alt tag jika berupa gambar.

5. Constraint Aset & Konten

    Gambar: Menggunakan layanan Unsplash CDN dengan parameter resize otomatis (q=80&w=800).
    Vektor: Ikon panah/rantai digambar manual menggunakan SVG inline path untuk menghindari dependensi library ikon (meningkatkan kecepatan load).
