Dokumentasi Desain & Narasi Visual: Landing Page "Berkarya Untuk Indonesia"
1. Filosofi & DNA Visual (Referensi: Axion Studio)

Desain ini mengadopsi pendekatan High-End Digital Agency yang dipopulerkan oleh studio-studio kelas dunia (referensi utama: Axion Studio). Karakteristik utama dari gaya ini adalah kesan premium yang diciptakan melalui pengekangan (restraint). Kita tidak menggunakan warna yang berteriak atau bentuk yang rumit. Sebaliknya, kita memaksimalkan ruang negatif (whitespace), tipografi yang sangat ketat dan raksasa, serta membiarkan mikro-interaksi yang halus menjadi pernyataan utama. 

Halaman ini tidak terlihat seperti brosur mahasiswa pada umumnya; halaman ini dirancang seolah-olah merupakan produk digital dari agensi besar yang menghargai detail piksel.
2. Anatomi Layout Global
Sistem Grid & Kontainer

Seluruh halaman dibatasi oleh kontainer maksimal lebar 1440px (max-w-[1440px]) yang berada di tengah layar. Di luar kontainer ini, layar akan diisi oleh warna latar belakang section tersebut, menciptakan kesan bahwa konten "mengapung" di dalam lajur yang terkontrol. Padding horizontal kontainer menggunakan sistem responsif: px-5 pada mobile, px-8 pada tablet, dan px-12 pada desktop, memastikan ruang napas yang cukup di layar manapun.
Navigasi (The Floating Pill)

Navigasi tidak menempel di tepi layar. Ia adalah elemen yang melayang (floating) di dalam kontainer, berbentuk kapsul/pil (rounded-full) dengan latar belakang putih solid dan bayangan yang sangat tipis. 

     Kiri: Logo hitam pekat berbentuk lingkaran dengan inisial putih. Diikuti oleh tautan navigasi yang sangat bersih (font-size 14px, warna gelap, yang memudar menjadi abu-abu saat di-hover dengan transisi 300ms).
     Kanan: Area utilitas. Terdapat jam live (timezones) sebagai sentuhan "tech-savvy", dan satu tombol CTA utama berwarna hitam peat. Tombol ini tidak statis; ia memiliki animasi text-roll vertikal dan ikon panah di dalam lingkaran putih yang berputar halus saat tombol di-hover.

3. Narasi Per-Section
Section 1: HERO (The Statement Maker)

Hero section bukan sekadar pengantar; ia adalah pernyataan utama yang menguasai seluruh viewport (100vh).

     Latar Belakang Dinamis (Shader Replacement): Alih-alih menggunakan latar belakang datar, kita menggunakan animasi gradien CSS yang sangat lambat dan halus. Ini meniru efek WebGL Shader yang memberikan kesan "hidup" dan organik pada latar belakang abu-abu muda, seolah-olah ada cahaya yang bergerak perlahan di balik kaca es.
     Penempatan Konten (Bottom-Aligned): Ini adalah kunci desain Axion. Konten hero TIDAK berada di tengah vertikal. Ia menempel di dasar viewport (flex flex-col justify-end). Ini menciptakan ruang negatif yang masif di bagian atas layar, memberikan kesan dramatis dan bernapas, sementara teks utama bertumpu dengan kokoh di bawah.
     Tipografi Raksasa: Headline menggunakan teknik Fluid Typography (clamp). Pada mobile, teks cukup besar (sekitar 28px), namun pada desktop ia mengembang hingga 67px (4.2rem). Tracking (jarak antar huruf) diperketat (-0.03em) agar teks yang sangat besar tetap terlihat kompak dan elegan. Pemisahan baris diatur secara manual: pada mobile teks mengalir natural, tetapi pada desktop ia dipaksa pindah baris menggunakan <br> tersembunyi untuk menciptakan ritme baca yang dramatis.
     CTA Row: Terdiri dari tombol Oranye utama dan badge partner berwarna putih. Keduanya sejajar secara horizontal di desktop, dan bertumpuk di mobile.
         Tombol Oranye: Memiliki efek Text Roll. Saat di-hover, teks di dalam tombol bergeser ke atas secara vertikal, digantikan oleh teks yang sama, menciptakan ilusi gulungan tak berujung. Di ujung kanan tombol, ada lingkaran putih berisi ikon panah yang berputar -45 derajat menjadi tegak lurus saat hover, menandakan arah tindakan.

Section 2: TENTANG PROGRAM (The Editorial Grid)

Bagian ini meninggalkan latar belakang abu-abu dan beralih ke putih bersih. Tujuannya adalah memberikan fokus penuh pada narasi dan aset visual.

     Label Pembuka: Dimulai dengan baris horizontal yang berisi lingkaran hitam berisi angka "1" dan label teks dalam kapsul border. Ini memberikan struktur indeks yang rapi.
     Headline: Sedikit lebih kecil dari Hero, namun tetap menggunakan ketatan (tracking) yang sama untuk konsistensi visual.
     Layout Asimetris (Desktop): Ini adalah flagship desainnya. Alih-alih grid yang kaku 50-50, kita menggunakan CSS Grid dengan proporsi 26% | 1fr | 48%.
         Kolom pertama (26%) berisi gambar vertikal kecil yang di-align ke bawah (self-end).
         Kolom kedua (1fr / fleksibel) berisi teks paragraf dan tombol, di-align ke atas (self-start dan justify-end), membiarkan teks mengapung di tengah-tengah tinggi visual.
         Kolom ketiga (48%) berisi gambar horizontal besar yang juga di-align ke bawah.
         Hasilnya: Sebuah komposisi editorial yang tidak simetris, sangat menarik secara visual, dan mematahkan kebosanan layout kotak-kotak. Pada mobile, ini dipecah menjadi tumpukan vertikal standar demi aksesibilitas.

Section 3: CALL TO ACTION (The Conversion Cards)

Latar belakang bergeser menjadi abu-abu terang yang sangat lembut (#F5F5F5), menandakan bahwa kita memasuki area aksi.

     Struktur Kartu: Alih-alih sekadar teks dan tombol besar, kita mengemas CTA ke dalam 2 kartu visual (mewakili Kreativitas dan Teknologi). Kartu ini memiliki rasio aspek yang berbeda (satu landscape, satu persegi) untuk menambah dinamika layout grid 2 kolom.
     Mekanisme Hover (The Expanding Pill): Ini adalah detail yang mencuri perhatian. Di atas gambar kartu, terdapat tombol melayang di pojok kiri bawah. Secara default, tombol ini hanyalah lingkaran kecil (36x36px) berisi ikon rantai/panah. Namun, saat pengguna meng-hover area kartu tersebut, lingkaran ini akan melebar secara horizontal (menggunakan transition-all duration-300) berubah menjadi kapsul/pil yang memuat teks "Gabung Sekarang". Teks tersebut muncul dari opacity 0 ke 1 dengan sedikit delay agar terlihat seperti sedang "terungkap". Efek ini memberikan kejutan visual yang sangat memuaskan (delightful) dan mendorong klik.

4. Kamus Animasi & Transisi (The Motion Language)

Agar konsisten, semua animasi menggunakan bahasa gerak yang sama:

     Easing: cubic-bezier(0.25, 0.1, 0.25, 1). Ini adalah kurva ease-out yang sangat lembut, membuat elemen bergerak terasa meluncur tanpa pantulan yang berlebihan.
     Durasi: Standar 300ms untuk pergerakan kecil (hover warna, rotasi ikon), dan 500ms untuk pergerakan besar (text-roll, perpindahan layout).
     Filosofi Gerak: Tidak ada yang instan. Semuanya terasa terhubung dan mengalir, mencerminkan filosofi "Berkarya" yang membutuhkan proses yang terarah dan bermakna.
