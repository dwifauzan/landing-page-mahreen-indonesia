Project Plan: Mahreen Indonesia Internship Test
1. Ringkasan Eksekutif

Proyek ini adalah pembuatan Landing Page bertema "Berkarya Untuk Indonesia" untuk memenuhi Tes Kompetensi Web Developer Mahreen Indonesia. Proyek ini menggunakan pendekatan Spec-Driven Development dengan arsitektur Single-File HTML untuk memaksimalkan kecepatan eksekusi, mengeliminasi risiko build-error, dan mempertahankan kualitas visual kelas atas (terinspirasi referensi desain agensi premium).
2. Timeline & Milestone (Target Penyelesaian: < 5 Jam)

    Milestone 1: Analisis & Arsitektur (T-05:00 - T-04:00)
        Kaji ulang brief, ekstrak constraint (3 section, batas kata, format submit).
        Keputusan arsitektur: Single-file HTML + Tailwind CDN.
        Penyusunan SRS dan Design Tokens.
    Milestone 2: Eksekusi Kode (T-04:00 - T-02:00)
        Pembuatan kerangka HTML.
        Implementasi komponen visual per section (Nav, Hero, Tentang, CTA).
        Implementasi Custom CSS (Animasi gradien, Text-roll).
        Implementasi Vanilla JS (Jam Jakarta).
    Milestone 3: QA & Polishing (T-02:00 - T-01:00)
        Audit responsivitas (Mobile, Tablet, Desktop).
        Pengujian cross-browser (Safari/Chrome).
        Optimasi aset dan cek Core Web Vitals visual.
    Milestone 4: Deployment & Submission (T-01:00 - T-00:00)
        Deploy via Netlify Drop.
        Eksekusi requirements administrasi (Screenshot, PDF, Instagram).

3. Manajemen Risiko & Mitigasi
Risiko	Dampak	Probabilitas	Mitigasi
Over-engineering (Pakai React/Vite)	Tinggi (Waktu habis, build error)	Rendah (Sudah diputuskan drop)	Patuh pada arsitektur HTML Tunggal. Tidak ada npm/node_modules.
Broken Link / 404 saat Deploy	Fatal (Diskualifikasi)	Sedang	Gunakan Netlify Drop (auto-deploy index.html), uji link di Incognito mode sebelum submit.
Pelanggaran Brief (Section berlebih)	Tinggi (Potongan nilai 25%)	Rendah	Strictly 3 section: Hero, Tentang, CTA. Tidak ada footer terpisah.
WebGL/Shader Gagal Render	Sedang (Visual rusak)	Tinggi (Jika pakai JS lib)	Ganti shader dengan CSS Gradient Animation yang 100% stabil di semua browser.
Aset Gambar Loading Lambat	Sedang (UI jatuh)	Sedang	Gunakan Unsplash URL dengan parameter w=800&q=80 untuk kompresi.
4. Strategi Penilaian (Scoring Alignment)

    Kreativitas (30%): Dicapai melalui animasi text-roll, layout grid asimetris, dan expanding pill button.
    Kesesuaian Brief (25%): Dipenuhi dengan ketat patuh pada 3 section dan batasan kata.
    Kualitas Hasil (25%): Dijamin melalui performa loading sangat cepat tanpa framework JS berat.
    Komunikasi Ide (10%): Dicapai melalui hirarki visual tipografi yang dramatis.
    Kerapihan (10%): Diterapkan melalui Semantic HTML dan penamaan class Tailwind yang konsisten.
