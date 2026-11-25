<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>SIWAS 28/2026 - Aplikasi Kerja & Analisis Tupoksi Pengawas Sekolah</title>
  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Google Fonts: Inter -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet" />
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'system-ui', 'sans-serif'],
          },
        },
      },
    };
  </script>
  <style>
    body {
      font-family: 'Inter', system-ui, sans-serif;
    }
    @media print {
      .no-print {
        display: none !important;
      }
      .print-only {
        display: block !important;
      }
      body {
        background: #ffffff !important;
        color: #0f172a !important;
      }
      .print-card {
        box-shadow: none !important;
        border: 1px solid #cbd5e1 !important;
        break-inside: avoid;
      }
    }
  </style>
</head>
<body class="bg-slate-50 text-slate-800 antialiased min-h-screen flex flex-col">

  <!-- ==================== LAYAR LOGIN NIP PENGAWAS ==================== -->
  <div id="loginOverlay" class="fixed inset-0 z-40 bg-slate-900/95 backdrop-blur-sm flex items-center justify-center p-4 no-print">
    <div class="bg-white rounded-3xl max-w-md w-full p-6 sm:p-8 shadow-2xl border border-slate-200 space-y-6">
      <!-- Logo (Klik 3x untuk membuka Panel Admin tersembunyi) -->
      <div class="text-center space-y-3">
        <div id="loginLogoTrigger" title="SIWAS 28/2026" class="w-16 h-16 mx-auto rounded-2xl bg-indigo-600 text-white flex items-center justify-center shadow-lg shadow-indigo-200 cursor-pointer select-none active:scale-95 transition">
          <svg class="w-9 h-9" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
          </svg>
        </div>
        <div>
          <h2 class="text-2xl font-extrabold text-slate-900 tracking-tight">SIWAS 28/2026</h2>
          <p class="text-xs text-slate-500 mt-1">Masuk menggunakan NIP Pengawas Sekolah terdaftar</p>
        </div>
      </div>

      <!-- Form Login NIP -->
      <form id="formLogin" class="space-y-4">
        <div>
          <label for="loginNipInput" class="block text-xs font-semibold text-slate-700 mb-1.5">Nomor Induk Pegawai (NIP)</label>
          <input type="text" id="loginNipInput" inputmode="numeric" required placeholder="Masukkan 18 digit NIP Anda..." class="w-full px-4 py-3 text-sm rounded-xl border border-slate-300 focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 outline-none tracking-wide" />
        </div>

        <!-- Pesan Error Inline -->
        <div id="loginErrorBox" class="hidden p-3 rounded-xl bg-rose-50 border border-rose-200 text-rose-700 text-xs font-medium">
          NIP tidak ditemukan. Hubungi Admin untuk mendaftarkan NIP Anda.
        </div>

        <button type="submit" class="w-full py-3 px-4 rounded-xl bg-indigo-600 hover:bg-indigo-700 text-white font-semibold text-sm shadow-sm transition flex items-center justify-center gap-2">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M11 16l-4-4m0 0l4-4m-4 4h14m-5 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h7a3 3 0 013 3v1" />
          </svg>
          Masuk Aplikasi
        </button>
      </form>

      <!-- Info NIP Demo -->
      <div class="pt-4 border-t border-slate-100 text-center space-y-1">
        <p class="text-[11px] text-slate-500">Contoh NIP bawaan untuk uji coba:</p>
        <p class="text-xs font-mono font-semibold text-indigo-600 select-all">197205141998021001</p>
      </div>
    </div>
  </div>

  <!-- ==================== HEADER / NAVBAR ==================== -->
  <header class="bg-white border-b border-slate-200 sticky top-0 z-30 no-print">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16 gap-3">
        <!-- Brand / Logo (Klik 3x untuk Panel Admin tersembunyi) -->
        <div id="headerLogoTrigger" class="flex items-center gap-3 min-w-0 cursor-pointer select-none" title="SIWAS 28/2026">
          <div class="w-10 h-10 rounded-xl bg-indigo-600 text-white flex items-center justify-center shadow-sm shrink-0 active:scale-95 transition">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
            </svg>
          </div>
          <div class="truncate">
            <h1 class="text-base sm:text-lg font-bold text-slate-900 leading-tight truncate">SIWAS 28/2026</h1>
            <p class="text-xs text-slate-500 truncate">Permendikdasmen No. 28 Tahun 2026 • Pengawas Sekolah</p>
          </div>
        </div>

        <!-- Tombol Tahun Pelajaran Manual, Profil & Keluar -->
        <div class="flex items-center gap-2 shrink-0">
          <!-- Tombol Tahun Pelajaran Manual -->
          <button id="btnOpenTp" type="button" title="Ubah Tahun Pelajaran secara manual" class="flex items-center gap-1.5 px-3 py-2 rounded-xl bg-indigo-50 hover:bg-indigo-100 text-indigo-700 border border-indigo-200 transition text-xs font-bold">
            <svg class="w-4 h-4 shrink-0" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
            </svg>
            <span class="hidden md:inline">Tahun Pelajaran:</span>
            <span id="headerTpLabel">2026/2027</span>
          </button>

          <!-- Profil Pengawas -->
          <button id="btnOpenProfile" type="button" class="flex items-center gap-2.5 px-3 py-2 rounded-xl bg-slate-100 hover:bg-slate-200 transition text-left">
            <div class="w-8 h-8 rounded-full bg-indigo-100 text-indigo-700 font-bold text-xs flex items-center justify-center" id="headerAvatar">PS</div>
            <div class="hidden sm:block max-w-[170px]">
              <p class="text-xs font-semibold text-slate-800 truncate" id="headerName">Pengawas Sekolah</p>
              <p class="text-[11px] text-indigo-600 font-medium truncate" id="headerRank">Ahli Madya (IV/a)</p>
            </div>
            <svg class="w-4 h-4 text-slate-400" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M15.232 5.232l3.536 3.536m-2.036-5.036a2.5 2.5 0 113.536 3.536L6.5 21.036H3v-3.572L16.732 3.732z" />
            </svg>
          </button>

          <!-- Tombol Keluar -->
          <button id="btnLogout" type="button" title="Keluar (Ganti NIP)" class="p-2.5 rounded-xl bg-rose-50 hover:bg-rose-100 text-rose-600 transition">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M17 16l4-4m0 0l-4-4m4 4H7m6 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h4a3 3 0 013 3v1" />
            </svg>
          </button>
        </div>
      </div>

      <!-- Navigasi Tab Responsif -->
      <nav class="flex gap-1 overflow-x-auto pb-2 pt-1 -mx-1 px-1" aria-label="Menu Utama">
        <button type="button" data-tab="analisis" class="nav-tab flex items-center gap-2 px-4 py-2.5 rounded-xl text-sm font-semibold whitespace-nowrap transition bg-indigo-600 text-white shadow-sm">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
          </svg>
          Analisis Tupoksi & Instrumen
        </button>
        <button type="button" data-tab="jurnal" class="nav-tab flex items-center gap-2 px-4 py-2.5 rounded-xl text-sm font-semibold whitespace-nowrap transition text-slate-600 hover:bg-slate-100">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4" />
          </svg>
          Jurnal Pengawasan
        </button>
        <button type="button" data-tab="sekolah" class="nav-tab flex items-center gap-2 px-4 py-2.5 rounded-xl text-sm font-semibold whitespace-nowrap transition text-slate-600 hover:bg-slate-100">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4" />
          </svg>
          Sekolah Binaan
        </button>
        <button type="button" data-tab="angkakredit" class="nav-tab flex items-center gap-2 px-4 py-2.5 rounded-xl text-sm font-semibold whitespace-nowrap transition text-slate-600 hover:bg-slate-100">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M9 7h6m0 10v-3m-3 3h.01M9 17h.01M9 14h.01M12 14h.01M15 11h.01M12 11h.01M9 11h.01M7 21h10a2 2 0 002-2V5a2 2 0 00-2-2H7a2 2 0 00-2 2v14a2 2 0 002 2z" />
          </svg>
          Kalkulator Angka Kredit
        </button>
      </nav>
    </div>
  </header>

  <!-- ==================== MAIN CONTENT ==================== -->
  <main class="flex-1 max-w-7xl w-full mx-auto px-4 sm:px-6 lg:px-8 py-6">

    <!-- Kop Cetak Global (Muncul saat Cetak) -->
    <div class="hidden print-only border-b-2 border-slate-800 pb-4 mb-6">
      <h2 class="text-xl font-bold text-center uppercase">Laporan Pengawasan Mutu Pendidikan</h2>
      <p class="text-xs text-center text-slate-600">Berdasarkan Permendikdasmen Nomor 28 Tahun 2026</p>
      <div class="grid grid-cols-2 gap-2 text-xs mt-4">
        <p><strong>Nama Pengawas:</strong> <span id="printName">-</span></p>
        <p><strong>NIP:</strong> <span id="printNip">-</span></p>
        <p><strong>Jenjang / Golongan:</strong> <span id="printRank">-</span></p>
        <p><strong>Instansi:</strong> <span id="printInstansi">-</span></p>
        <p class="col-span-2"><strong>Tahun Pelajaran:</strong> <span id="printTp">2026/2027</span></p>
      </div>
    </div>

    <!-- ========================================================== -->
    <!-- TAB 1: ANALISIS TUPOKSI & INSTRUMEN 16 INDIKATOR           -->
    <!-- ========================================================== -->
    <section id="tab-analisis" class="tab-panel space-y-6">
      <!-- Banner Ringkasan Regulasi -->
      <div class="bg-gradient-to-br from-indigo-700 via-indigo-600 to-blue-600 rounded-2xl p-6 sm:p-8 text-white shadow-md no-print">
        <div class="flex flex-col lg:flex-row lg:items-center lg:justify-between gap-6">
          <div class="space-y-2 max-w-3xl">
            <span class="inline-flex items-center px-3 py-1 rounded-full text-xs font-semibold bg-white/15 text-indigo-50 backdrop-blur-sm">
              Dasar Hukum: Permendikdasmen No. 28 Tahun 2026 (Berlaku 16 Nov 2026)
            </span>
            <h2 class="text-2xl sm:text-3xl font-extrabold tracking-tight">
              Analisis Tupoksi & Instrumen Pengawas Sekolah
            </h2>
            <p class="text-sm sm:text-base text-indigo-100 leading-relaxed">
              Mencabut Permendikbud 143/2014 dan menindaklanjuti PermenPANRB No. 7 Tahun 2026. JF Pengawas Sekolah berdiri sebagai jabatan fungsional mandiri kategori keahlian dengan fokus pengawasan mutu melalui <strong>Pemantauan, Penilaian, dan Pembinaan</strong> dalam <strong>Tim Kerja</strong> pada Satuan Pendidikan formal (PAUD, Dikdas, Dikmen).
            </p>
          </div>
          <div class="grid grid-cols-2 gap-3 shrink-0">
            <div class="bg-white/10 backdrop-blur-sm rounded-xl p-3.5 border border-white/15">
              <p class="text-xs text-indigo-100">Jenjang Jabatan</p>
              <p class="text-lg font-bold">3 Jenjang</p>
              <p class="text-[11px] text-indigo-200">Muda • Madya • Utama</p>
            </div>
            <div class="bg-white/10 backdrop-blur-sm rounded-xl p-3.5 border border-white/15">
              <p class="text-xs text-indigo-100">Indikator Kegiatan</p>
              <p class="text-lg font-bold">16 Butir</p>
              <p class="text-[11px] text-indigo-200">Lampiran I Bagian C</p>
            </div>
          </div>
        </div>
      </div>

      <!-- 4 Poin Kunci Perubahan & Kedudukan -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4 no-print">
        <div class="bg-white rounded-2xl p-5 border border-slate-200 shadow-sm">
          <div class="w-10 h-10 rounded-xl bg-blue-50 text-blue-600 flex items-center justify-center mb-3">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5" />
            </svg>
          </div>
          <h3 class="font-bold text-slate-900 text-sm mb-1">Kedudukan & Atasan (Pasal 4 & 38)</h3>
          <p class="text-xs text-slate-600 leading-relaxed">
            Pelaksana teknis fungsional pengawasan mutu pada satuan pendidikan formal. Bertanggung jawab dan dinilai kinerjanya oleh <strong>Pejabat Pimpinan Tinggi Pratama (Kepala Dinas Pendidikan)</strong>.
          </p>
        </div>

        <div class="bg-white rounded-2xl p-5 border border-slate-200 shadow-sm">
          <div class="w-10 h-10 rounded-xl bg-emerald-50 text-emerald-600 flex items-center justify-center mb-3">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0z" />
            </svg>
          </div>
          <h3 class="font-bold text-slate-900 text-sm mb-1">Pola Tim Kerja (Pasal 11 & 38)</h3>
          <p class="text-xs text-slate-600 leading-relaxed">
            Tugas dilaksanakan dalam <strong>tim kerja</strong> berbasis keahlian & kolaborasi. Kepala Dinas dapat menugaskan Pengawas ke dalam <strong>Tim Kinerja Kepala Sekolah</strong> untuk memantau, membina, dan merekomendasikan penilaian KS.
          </p>
        </div>

        <div class="bg-white rounded-2xl p-5 border border-slate-200 shadow-sm">
          <div class="w-10 h-10 rounded-xl bg-amber-50 text-amber-600 flex items-center justify-center mb-3">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253" />
            </svg>
          </div>
          <h3 class="font-bold text-slate-900 text-sm mb-1">Arah Pembelajaran & Mutu</h3>
          <p class="text-xs text-slate-600 leading-relaxed">
            Menekankan peningkatan <strong>Rapor Pendidikan</strong> (literasi, numerasi, karakter), budaya karakter dalam manajemen, serta pembelajaran <strong>berkesadaran, bermakna, dan menggembirakan</strong>.
          </p>
        </div>

        <div class="bg-white rounded-2xl p-5 border border-slate-200 shadow-sm">
          <div class="w-10 h-10 rounded-xl bg-purple-50 text-purple-600 flex items-center justify-center mb-3">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z" />
            </svg>
          </div>
          <h3 class="font-bold text-slate-900 text-sm mb-1">Nomenklatur & Karier (Pasal 80 & 88)</h3>
          <p class="text-xs text-slate-600 leading-relaxed">
            Nomenklatur diseragamkan menjadi <em>Ahli Muda, Madya, Utama</em> (tanpa embel-embel jenjang sekolah). Tidak ada pengangkatan pertama; wajib Sertifikat Pendidik, dan minimal <strong>S-2</strong> untuk Ahli Utama.
          </p>
        </div>
      </div>

      <!-- Matriks Perbedaan Fokus 3 Jenjang -->
      <div class="bg-white rounded-2xl border border-slate-200 shadow-sm overflow-hidden no-print">
        <div class="p-5 border-b border-slate-200">
          <h3 class="text-base font-bold text-slate-900">Matriks Perbedaan Ruang Lingkup per Jenjang</h3>
          <p class="text-xs text-slate-500">Klik jenjang di bawah untuk menampilkan & menilai 16 indikator cakupan kegiatan sesuai Lampiran I Bagian C.</p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 divide-y md:divide-y-0 md:divide-x divide-slate-200">
          <button type="button" onclick="selectAnalysisJenjang('muda')" id="card-jenjang-muda" class="jenjang-card text-left p-5 transition hover:bg-indigo-50/50 focus:outline-none">
            <div class="flex items-center justify-between mb-2">
              <span class="px-2.5 py-1 rounded-lg text-xs font-bold bg-sky-100 text-sky-700">Ahli Muda (III/c - III/d)</span>
              <span class="text-xs font-semibold text-slate-500">AK: 25/thn</span>
            </div>
            <h4 class="font-bold text-slate-900 text-sm mb-1">Fokus: Analisis Mutu</h4>
            <p class="text-xs text-slate-600 leading-relaxed mb-2">
              Melakukan analisis mutu melalui pengawasan manajerial dan akademik pada Satuan Pendidikan formal.
            </p>
            <p class="text-[11px] font-medium text-sky-700 bg-sky-50 px-2.5 py-1.5 rounded-lg">
              Ciri Khas PKB: Komunitas Belajar di dalam Satuan Pendidikan.
            </p>
          </button>

          <button type="button" onclick="selectAnalysisJenjang('madya')" id="card-jenjang-madya" class="jenjang-card text-left p-5 transition hover:bg-indigo-50/50 focus:outline-none ring-2 ring-inset ring-indigo-600 bg-indigo-50/40">
            <div class="flex items-center justify-between mb-2">
              <span class="px-2.5 py-1 rounded-lg text-xs font-bold bg-indigo-100 text-indigo-700">Ahli Madya (IV/a - IV/c)</span>
              <span class="text-xs font-semibold text-slate-500">AK: 37,5/thn</span>
            </div>
            <h4 class="font-bold text-slate-900 text-sm mb-1">Fokus: Pengendalian & Pengembangan Mutu</h4>
            <p class="text-xs text-slate-600 leading-relaxed mb-2">
              Melakukan pengendalian dan pengembangan mutu melalui pengawasan manajerial dan akademik pada Satuan Pendidikan formal.
            </p>
            <p class="text-[11px] font-medium text-indigo-700 bg-indigo-100/70 px-2.5 py-1.5 rounded-lg">
              Ciri Khas PKB: Kolaborasi lintas Satuan Pendidikan.
            </p>
          </button>

          <button type="button" onclick="selectAnalysisJenjang('utama')" id="card-jenjang-utama" class="jenjang-card text-left p-5 transition hover:bg-indigo-50/50 focus:outline-none">
            <div class="flex items-center justify-between mb-2">
              <span class="px-2.5 py-1 rounded-lg text-xs font-bold bg-purple-100 text-purple-700">Ahli Utama (IV/d - IV/e)</span>
              <span class="text-xs font-semibold text-slate-500">AK: 50/thn</span>
            </div>
            <h4 class="font-bold text-slate-900 text-sm mb-1">Fokus: Strategis & Inovasi Sistem</h4>
            <p class="text-xs text-slate-600 leading-relaxed mb-2">
              Melakukan kegiatan strategis dan inovasi pengembangan sistem pengawasan manajerial dan akademik.
            </p>
            <p class="text-[11px] font-medium text-purple-700 bg-purple-50 px-2.5 py-1.5 rounded-lg">
              Ciri Khas PKB: Jejaring kolaborasi lintas wilayah/instansi (Wajib S-2).
            </p>
          </button>
        </div>
      </div>

      <!-- Instrumen Penilaian 16 Indikator (Skor 1-4 + Keterangan + Bukti Dukung) -->
      <div class="bg-white rounded-2xl border border-slate-200 shadow-sm p-5 sm:p-6 space-y-5">
        <div class="flex flex-col lg:flex-row lg:items-center justify-between gap-4 border-b border-slate-100 pb-4">
          <div>
            <h3 class="text-base font-bold text-slate-900" id="analysisTitle">Instrumen 16 Indikator: Pengawas Sekolah Ahli Madya</h3>
            <p class="text-xs text-slate-500 mt-0.5" id="analysisSubtitle">Lampiran I Bagian C Permendikdasmen No. 28 Tahun 2026</p>
          </div>
          <!-- Pilih Sekolah Binaan & Aksi Ekspor/Cetak -->
          <div class="flex flex-wrap items-center gap-2 no-print">
            <select id="instrumenSchoolSelect" class="px-3 py-2 text-xs sm:text-sm rounded-xl border border-slate-300 bg-white font-medium text-slate-700 focus:ring-2 focus:ring-indigo-500 outline-none">
              <!-- Diisi dari daftar sekolah binaan -->
            </select>
            <button type="button" onclick="exportInstrumenCSV()" class="px-3 py-2 rounded-xl bg-slate-100 hover:bg-slate-200 text-slate-700 text-xs font-semibold transition flex items-center gap-1.5">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4" />
              </svg>
              Unduh CSV
            </button>
            <button type="button" onclick="window.print()" class="px-3 py-2 rounded-xl bg-indigo-50 hover:bg-indigo-100 text-indigo-700 text-xs font-semibold transition flex items-center gap-1.5">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M17 17h2a2 2 0 002-2v-4a2 2 0 00-2-2H5a2 2 0 00-2 2v4a2 2 0 002 2h2m2 4h6a2 2 0 002-2v-4a2 2 0 00-2-2H9a2 2 0 00-2 2v4a2 2 0 002 2zm8-12V5a2 2 0 00-2-2H9a2 2 0 00-2 2v4h10z" />
              </svg>
              Cetak
            </button>
          </div>
        </div>

        <!-- Ringkasan Skor Instrumen & Filter Pilar -->
        <div class="grid grid-cols-1 md:grid-cols-4 gap-3 bg-slate-50 rounded-xl p-4 border border-slate-200">
          <div>
            <p class="text-[11px] font-semibold text-slate-500 uppercase">Sekolah & Tahun Pelajaran</p>
            <p class="text-xs sm:text-sm font-bold text-slate-900 mt-0.5 truncate" id="instrumenSummarySchool">-</p>
            <p class="text-[11px] font-semibold text-indigo-600" id="instrumenSummaryTp">TP 2026/2027</p>
          </div>
          <div>
            <p class="text-[11px] font-semibold text-slate-500 uppercase">Indikator Dinilai</p>
            <p class="text-xl font-extrabold text-slate-900 mt-0.5"><span id="instrumenCountFilled">0</span> <span class="text-xs font-medium text-slate-400">/ 16</span></p>
          </div>
          <div>
            <p class="text-[11px] font-semibold text-slate-500 uppercase">Rata-rata Skor</p>
            <p class="text-xl font-extrabold text-indigo-700 mt-0.5" id="instrumenAvgScore">0,00</p>
          </div>
          <div>
            <p class="text-[11px] font-semibold text-slate-500 uppercase">Predikat Mutu</p>
            <div class="mt-1" id="instrumenPredikatBadge">
              <span class="px-2.5 py-1 rounded-lg text-xs font-bold bg-slate-200 text-slate-600">Belum Dinilai</span>
            </div>
          </div>
        </div>

        <!-- Filter Pilar & Panduan Rubrik -->
        <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-3 no-print">
          <div class="flex flex-wrap gap-2">
            <button type="button" onclick="setPillarFilter('all')" class="pillar-btn px-3 py-1.5 rounded-lg text-xs font-semibold bg-slate-900 text-white" data-pillar="all">Semua (16)</button>
            <button type="button" onclick="setPillarFilter('pemantauan')" class="pillar-btn px-3 py-1.5 rounded-lg text-xs font-semibold bg-slate-100 text-slate-600 hover:bg-slate-200" data-pillar="pemantauan">1. Pemantauan (5)</button>
            <button type="button" onclick="setPillarFilter('penilaian')" class="pillar-btn px-3 py-1.5 rounded-lg text-xs font-semibold bg-slate-100 text-slate-600 hover:bg-slate-200" data-pillar="penilaian">2. Penilaian (6)</button>
            <button type="button" onclick="setPillarFilter('pembinaan')" class="pillar-btn px-3 py-1.5 rounded-lg text-xs font-semibold bg-slate-100 text-slate-600 hover:bg-slate-200" data-pillar="pembinaan">3. Pembinaan (5)</button>
          </div>
          <p class="text-[11px] text-slate-500">Pilih skor <strong>1–4</strong> & isi <strong>Bukti Dukung</strong> langsung pada tiap indikator (tersimpan otomatis).</p>
        </div>

        <!-- Daftar 16 Indikator dengan Skor 1,2,3,4 + Keterangan + Kolom Bukti Dukung -->
        <div id="tupoksiListContainer" class="space-y-5">
          <!-- Diisi dinamis oleh JS -->
        </div>
      </div>
    </section>

    <!-- ========================================================== -->
    <!-- TAB 2: JURNAL & CATATAN PENGAWASAN                         -->
    <!-- ========================================================== -->
    <section id="tab-jurnal" class="tab-panel hidden space-y-6">
      <!-- Ringkasan Statistik Jurnal -->
      <div class="grid grid-cols-2 lg:grid-cols-4 gap-4 no-print">
        <div class="bg-white rounded-2xl p-4 border border-slate-200 shadow-sm">
          <p class="text-xs font-medium text-slate-500">Total Kegiatan</p>
          <p class="text-2xl font-extrabold text-slate-900 mt-1" id="statTotal">0</p>
        </div>
        <div class="bg-white rounded-2xl p-4 border border-slate-200 shadow-sm">
          <p class="text-xs font-medium text-blue-600">Pemantauan</p>
          <p class="text-2xl font-extrabold text-blue-700 mt-1" id="statPemantauan">0</p>
        </div>
        <div class="bg-white rounded-2xl p-4 border border-slate-200 shadow-sm">
          <p class="text-xs font-medium text-amber-600">Penilaian</p>
          <p class="text-2xl font-extrabold text-amber-700 mt-1" id="statPenilaian">0</p>
        </div>
        <div class="bg-white rounded-2xl p-4 border border-slate-200 shadow-sm">
          <p class="text-xs font-medium text-emerald-600">Pembinaan</p>
          <p class="text-2xl font-extrabold text-emerald-700 mt-1" id="statPembinaan">0</p>
        </div>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-12 gap-6 items-start">
        <!-- Form Tambah Kegiatan Pengawasan -->
        <div class="lg:col-span-5 bg-white rounded-2xl border border-slate-200 shadow-sm p-5 sm:p-6 no-print">
          <h3 class="text-base font-bold text-slate-900 mb-1">Catat Kegiatan Pengawasan</h3>
          <p class="text-xs text-slate-500 mb-4">Terintegrasi dengan 16 butir cakupan kegiatan Permendikdasmen 28/2026.</p>

          <form id="formLog" class="space-y-4">
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
              <div>
                <label class="block text-xs font-semibold text-slate-700 mb-1">Tanggal</label>
                <input type="date" id="logDate" required class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 outline-none" />
              </div>
              <div>
                <label class="block text-xs font-semibold text-slate-700 mb-1">Sekolah Binaan</label>
                <select id="logSchool" required class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 outline-none bg-white">
                  <!-- Diisi dari daftar sekolah -->
                </select>
              </div>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
              <div>
                <label class="block text-xs font-semibold text-slate-700 mb-1">Pilar Pengawasan</label>
                <select id="logPillar" required class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 outline-none bg-white">
                  <option value="pemantauan">1. Pemantauan</option>
                  <option value="penilaian">2. Penilaian</option>
                  <option value="pembinaan">3. Pembinaan Manajerial & Akademik</option>
                </select>
              </div>
              <div>
                <label class="block text-xs font-semibold text-slate-700 mb-1">Status Pelaksanaan</label>
                <select id="logStatus" required class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 outline-none bg-white">
                  <option value="Terlaksana">Terlaksana</option>
                  <option value="Direncanakan">Direncanakan</option>
                  <option value="Tindak Lanjut Selesai">Tindak Lanjut Selesai</option>
                </select>
              </div>
            </div>

            <div>
              <label class="block text-xs font-semibold text-slate-700 mb-1">Butir Cakupan Kegiatan (Lampiran I)</label>
              <select id="logIndicator" required class="w-full px-3 py-2.5 text-xs sm:text-sm rounded-xl border border-slate-300 focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 outline-none bg-white">
                <!-- Diisi dinamis berdasarkan pilar & jenjang profil -->
              </select>
            </div>

            <!-- Skor Indikator 1, 2, 3, 4 beserta Keterangan -->
            <div>
              <label class="block text-xs font-semibold text-slate-700 mb-1.5">Skor Capaian Indikator (1 – 4)</label>
              <div class="grid grid-cols-2 gap-2" id="scoreRadioGroup">
                <label class="cursor-pointer">
                  <input type="radio" name="logScore" value="1" class="peer sr-only" />
                  <div class="p-2.5 rounded-xl border border-slate-200 bg-slate-50 peer-checked:bg-rose-50 peer-checked:border-rose-500 peer-checked:ring-1 peer-checked:ring-rose-500 transition">
                    <div class="flex items-center gap-1.5">
                      <span class="w-5 h-5 rounded-md bg-rose-100 text-rose-700 font-extrabold text-xs flex items-center justify-center">1</span>
                      <span class="text-xs font-bold text-slate-800">Kurang</span>
                    </div>
                    <p class="text-[10px] text-slate-500 mt-1 leading-snug">Belum memenuhi standar; perlu pembinaan intensif.</p>
                  </div>
                </label>
                <label class="cursor-pointer">
                  <input type="radio" name="logScore" value="2" class="peer sr-only" />
                  <div class="p-2.5 rounded-xl border border-slate-200 bg-slate-50 peer-checked:bg-amber-50 peer-checked:border-amber-500 peer-checked:ring-1 peer-checked:ring-amber-500 transition">
                    <div class="flex items-center gap-1.5">
                      <span class="w-5 h-5 rounded-md bg-amber-100 text-amber-700 font-extrabold text-xs flex items-center justify-center">2</span>
                      <span class="text-xs font-bold text-slate-800">Cukup</span>
                    </div>
                    <p class="text-[10px] text-slate-500 mt-1 leading-snug">Sebagian terpenuhi; perlu perbaikan terarah.</p>
                  </div>
                </label>
                <label class="cursor-pointer">
                  <input type="radio" name="logScore" value="3" class="peer sr-only" checked />
                  <div class="p-2.5 rounded-xl border border-slate-200 bg-slate-50 peer-checked:bg-blue-50 peer-checked:border-blue-500 peer-checked:ring-1 peer-checked:ring-blue-500 transition">
                    <div class="flex items-center gap-1.5">
                      <span class="w-5 h-5 rounded-md bg-blue-100 text-blue-700 font-extrabold text-xs flex items-center justify-center">3</span>
                      <span class="text-xs font-bold text-slate-800">Baik</span>
                    </div>
                    <p class="text-[10px] text-slate-500 mt-1 leading-snug">Memenuhi Standar Nasional Pendidikan (SNP).</p>
                  </div>
                </label>
                <label class="cursor-pointer">
                  <input type="radio" name="logScore" value="4" class="peer sr-only" />
                  <div class="p-2.5 rounded-xl border border-slate-200 bg-slate-50 peer-checked:bg-emerald-50 peer-checked:border-emerald-500 peer-checked:ring-1 peer-checked:ring-emerald-500 transition">
                    <div class="flex items-center gap-1.5">
                      <span class="w-5 h-5 rounded-md bg-emerald-100 text-emerald-700 font-extrabold text-xs flex items-center justify-center">4</span>
                      <span class="text-xs font-bold text-slate-800">Sangat Baik</span>
                    </div>
                    <p class="text-[10px] text-slate-500 mt-1 leading-snug">Melampaui standar, konsisten & inovatif.</p>
                  </div>
                </label>
              </div>
            </div>

            <div>
              <label class="block text-xs font-semibold text-slate-700 mb-1">Temuan / Hasil Pengamatan</label>
              <textarea id="logFinding" rows="2" required placeholder="Contoh: RPP guru belum mengintegrasikan pembelajaran berkesadaran dan asesmen formatif..." class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 outline-none"></textarea>
            </div>

            <div>
              <label class="block text-xs font-semibold text-slate-700 mb-1">Rekomendasi / Rencana Tindak Lanjut (RTL)</label>
              <textarea id="logRtl" rows="2" required placeholder="Contoh: Pendampingan komunitas belajar sekolah terkait pembelajaran mendalam & numerasi..." class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 outline-none"></textarea>
            </div>

            <!-- Kolom Bukti Dukung -->
            <div>
              <label class="block text-xs font-semibold text-slate-700 mb-1">Bukti Dukung (Dokumen / Tautan URL)</label>
              <input type="text" id="logEvidence" placeholder="Contoh: Foto supervisi, Berita Acara, atau https://drive.google.com/..." class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 outline-none" />
              <p class="text-[11px] text-slate-400 mt-1">Jika berupa tautan (http/https), otomatis dapat diklik pada daftar riwayat.</p>
            </div>

            <button type="submit" class="w-full py-3 px-4 rounded-xl bg-indigo-600 hover:bg-indigo-700 text-white font-semibold text-sm shadow-sm transition flex items-center justify-center gap-2">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 4v16m8-8H4" />
              </svg>
              Simpan ke Jurnal Pengawasan
            </button>
          </form>
        </div>

        <!-- Daftar Riwayat Jurnal Pengawasan -->
        <div class="lg:col-span-7 bg-white rounded-2xl border border-slate-200 shadow-sm p-5 sm:p-6">
          <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-3 mb-4 no-print">
            <div>
              <h3 class="text-base font-bold text-slate-900">Riwayat & Bukti Kinerja Pengawasan</h3>
              <p class="text-xs text-slate-500">Sebagai bahan pendokumentasian kinerja SKP (Pasal 41 ayat 2).</p>
            </div>
            <div class="flex flex-wrap gap-2">
              <button type="button" onclick="exportLogsCSV()" class="px-3 py-2 rounded-xl bg-slate-100 hover:bg-slate-200 text-slate-700 text-xs font-semibold transition flex items-center gap-1.5">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4" />
                </svg>
                Unduh CSV
              </button>
              <button type="button" onclick="window.print()" class="px-3 py-2 rounded-xl bg-indigo-50 hover:bg-indigo-100 text-indigo-700 text-xs font-semibold transition flex items-center gap-1.5">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M17 17h2a2 2 0 002-2v-4a2 2 0 00-2-2H5a2 2 0 00-2 2v4a2 2 0 002 2h2m2 4h6a2 2 0 002-2v-4a2 2 0 00-2-2H9a2 2 0 00-2 2v4a2 2 0 002 2zm8-12V5a2 2 0 00-2-2H9a2 2 0 00-2 2v4h10z" />
                </svg>
                Cetak Laporan
              </button>
            </div>
          </div>

          <!-- Filter Pencarian Jurnal -->
          <div class="grid grid-cols-1 sm:grid-cols-2 gap-3 mb-4 no-print">
            <input type="text" id="searchLog" placeholder="Cari sekolah, tahun pelajaran, bukti dukung, temuan..." class="w-full px-3 py-2 text-xs sm:text-sm rounded-xl border border-slate-200 focus:ring-2 focus:ring-indigo-500 outline-none" />
            <select id="filterLogPillar" class="w-full px-3 py-2 text-xs sm:text-sm rounded-xl border border-slate-200 focus:ring-2 focus:ring-indigo-500 outline-none bg-white">
              <option value="all">Semua Pilar Pengawasan</option>
              <option value="pemantauan">1. Pemantauan</option>
              <option value="penilaian">2. Penilaian</option>
              <option value="pembinaan">3. Pembinaan</option>
            </select>
          </div>

          <!-- List Jurnal -->
          <div id="logListContainer" class="space-y-3">
            <!-- Diisi dinamis oleh JS -->
          </div>
        </div>
      </div>
    </section>

    <!-- ========================================================== -->
    <!-- TAB 3: DATA SEKOLAH BINAAN                                 -->
    <!-- ========================================================== -->
    <section id="tab-sekolah" class="tab-panel hidden space-y-6">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-6 items-start">
        <!-- Form Tambah Sekolah Binaan -->
        <div class="lg:col-span-4 bg-white rounded-2xl border border-slate-200 shadow-sm p-5 sm:p-6">
          <h3 class="text-base font-bold text-slate-900 mb-1">Tambah Sekolah Binaan</h3>
          <p class="text-xs text-slate-500 mb-4">Kelola daftar satuan pendidikan formal binaan beserta prioritas Rapor Pendidikannya.</p>

          <form id="formSchool" class="space-y-3.5">
            <div>
              <label class="block text-xs font-semibold text-slate-700 mb-1">Nama Satuan Pendidikan</label>
              <input type="text" id="schoolName" required placeholder="Contoh: SDN 1 Wonogiri" class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 focus:ring-2 focus:ring-indigo-500 outline-none" />
            </div>
            <div class="grid grid-cols-2 gap-3">
              <div>
                <label class="block text-xs font-semibold text-slate-700 mb-1">Jenjang</label>
                <select id="schoolLevel" class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 bg-white outline-none">
                  <option value="PAUD/TK">PAUD / TK</option>
                  <option value="SD" selected>SD</option>
                  <option value="SMP">SMP</option>
                  <option value="SMA">SMA</option>
                  <option value="SMK">SMK</option>
                  <option value="SLB">SLB</option>
                </select>
              </div>
              <div>
                <label class="block text-xs font-semibold text-slate-700 mb-1">NPSN</label>
                <input type="text" id="schoolNpsn" placeholder="203xxxxx" class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 focus:ring-2 focus:ring-indigo-500 outline-none" />
              </div>
            </div>
            <div>
              <label class="block text-xs font-semibold text-slate-700 mb-1">Nama Kepala Sekolah</label>
              <input type="text" id="schoolPrincipal" required placeholder="Nama lengkap & gelar" class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 focus:ring-2 focus:ring-indigo-500 outline-none" />
            </div>
            <div>
              <label class="block text-xs font-semibold text-slate-700 mb-1">Prioritas Rapor Pendidikan</label>
              <select id="schoolPriority" class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 bg-white outline-none">
                <option value="Penguatan Literasi & Numerasi">Penguatan Literasi & Numerasi</option>
                <option value="Penguatan Karakter & Iklim Aman">Penguatan Karakter & Iklim Aman</option>
                <option value="Peningkatan Kualitas Pembelajaran">Peningkatan Kualitas Pembelajaran</option>
                <option value="Pengelolaan SNP & Kepemimpinan">Pengelolaan SNP & Kepemimpinan</option>
              </select>
            </div>
            <button type="submit" class="w-full py-3 px-4 rounded-xl bg-indigo-600 hover:bg-indigo-700 text-white font-semibold text-sm shadow-sm transition">
              + Tambahkan Sekolah Binaan
            </button>
          </form>
        </div>

        <!-- Daftar Sekolah Binaan -->
        <div class="lg:col-span-8 bg-white rounded-2xl border border-slate-200 shadow-sm p-5 sm:p-6">
          <div class="flex items-center justify-between mb-4">
            <div>
              <h3 class="text-base font-bold text-slate-900">Daftar Satuan Pendidikan Binaan</h3>
              <p class="text-xs text-slate-500">Digunakan pada Instrumen 16 Indikator dan Jurnal Pengawasan.</p>
            </div>
            <span class="px-3 py-1 rounded-full bg-indigo-50 text-indigo-700 text-xs font-bold" id="schoolCountBadge">0 Sekolah</span>
          </div>
          <div id="schoolListContainer" class="grid grid-cols-1 sm:grid-cols-2 gap-3.5">
            <!-- Diisi dinamis oleh JS -->
          </div>
        </div>
      </div>
    </section>

    <!-- ========================================================== -->
    <!-- TAB 4: KALKULATOR ANGKA KREDIT & SIMULASI KARIER           -->
    <!-- ========================================================== -->
    <section id="tab-angkakredit" class="tab-panel hidden space-y-6">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-6 items-start">
        <!-- Konfigurasi & Input Konversi Kinerja -->
        <div class="lg:col-span-5 space-y-5">
          <div class="bg-white rounded-2xl border border-slate-200 shadow-sm p-5 sm:p-6 space-y-4">
            <div>
              <h3 class="text-base font-bold text-slate-900">Parameter Jenjang & Pangkat</h3>
              <p class="text-xs text-slate-500">Mengacu pada Pasal 44–46, Pasal 68, dan Lampiran II Permendikdasmen 28/2026.</p>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
              <div>
                <label class="block text-xs font-semibold text-slate-700 mb-1">Jenjang Pengawas</label>
                <select id="akJenjang" class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 bg-white outline-none focus:ring-2 focus:ring-indigo-500">
                  <option value="muda">Ahli Muda (Koef. 25)</option>
                  <option value="madya" selected>Ahli Madya (Koef. 37,5)</option>
                  <option value="utama">Ahli Utama (Koef. 50)</option>
                </select>
              </div>
              <div>
                <label class="block text-xs font-semibold text-slate-700 mb-1">AK Awal Dimiliki</label>
                <input type="number" step="0.01" min="0" id="akInitial" value="0" class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 outline-none focus:ring-2 focus:ring-indigo-500" />
              </div>
            </div>

            <label class="flex items-start gap-3 p-3 rounded-xl bg-slate-50 border border-slate-200 cursor-pointer">
              <input type="checkbox" id="akEducationBonus" class="mt-0.5 w-4 h-4 rounded text-indigo-600 focus:ring-indigo-500" />
              <div>
                <span class="block text-xs font-semibold text-slate-800">Tambahan Ijazah Lebih Tinggi (Pasal 46)</span>
                <span class="block text-[11px] text-slate-500">+25% dari AK Kumulatif Kenaikan Pangkat (syarat kinerja min. Baik, 1x penilaian).</span>
              </div>
            </label>
          </div>

          <!-- Tambah Baris Penilaian Kinerja -->
          <div class="bg-white rounded-2xl border border-slate-200 shadow-sm p-5 sm:p-6">
            <h3 class="text-base font-bold text-slate-900 mb-1">Tambah Konversi Predikat Kinerja</h3>
            <p class="text-xs text-slate-500 mb-4">Mendukung penilaian tahunan (12 bulan) maupun periodik/proporsional (Pasal 45 ayat 3).</p>

            <form id="formAkPeriod" class="space-y-3.5">
              <div class="grid grid-cols-2 gap-3">
                <div>
                  <label class="block text-xs font-semibold text-slate-700 mb-1">Tahun / Label</label>
                  <input type="text" id="akYearLabel" value="2026" required class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 outline-none focus:ring-2 focus:ring-indigo-500" />
                </div>
                <div>
                  <label class="block text-xs font-semibold text-slate-700 mb-1">Periode (Bulan)</label>
                  <input type="number" id="akMonths" min="1" max="12" value="12" required class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 outline-none focus:ring-2 focus:ring-indigo-500" />
                </div>
              </div>
              <div>
                <label class="block text-xs font-semibold text-slate-700 mb-1">Predikat Kinerja</label>
                <select id="akPredikat" class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 bg-white outline-none focus:ring-2 focus:ring-indigo-500">
                  <option value="1.5">Sangat Baik (150%)</option>
                  <option value="1.0" selected>Baik (100%)</option>
                  <option value="0.75">Butuh Perbaikan / Cukup (75%)</option>
                  <option value="0.5">Kurang (50%)</option>
                  <option value="0.25">Sangat Kurang (25%)</option>
                </select>
              </div>
              <button type="submit" class="w-full py-2.5 px-4 rounded-xl bg-indigo-600 hover:bg-indigo-700 text-white font-semibold text-sm transition shadow-sm">
                + Tambah Periode Penilaian
              </button>
            </form>
          </div>
        </div>

        <!-- Hasil Perhitungan & Progres Kenaikan Pangkat / Jenjang -->
        <div class="lg:col-span-7 space-y-5">
          <div class="bg-white rounded-2xl border border-slate-200 shadow-sm p-5 sm:p-6 space-y-5">
            <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-3 border-b border-slate-100 pb-4">
              <div>
                <p class="text-xs font-semibold uppercase tracking-wider text-indigo-600">Total Akumulasi Angka Kredit</p>
                <p class="text-4xl font-extrabold text-slate-900 mt-1" id="akTotalDisplay">0,00</p>
              </div>
              <div class="text-left sm:text-right text-xs text-slate-500 space-y-0.5">
                <p>Koefisien Tahunan: <strong class="text-slate-800" id="akKoefDisplay">37,5</strong></p>
                <p>Bonus Pendidikan: <strong class="text-emerald-600" id="akBonusDisplay">+0,00</strong></p>
              </div>
            </div>

            <!-- Progress Kenaikan Pangkat -->
            <div class="space-y-1.5">
              <div class="flex justify-between text-xs font-semibold">
                <span class="text-slate-700">Target Kenaikan Pangkat (1 Tingkat)</span>
                <span id="akKpText" class="text-indigo-700">0 / 150</span>
              </div>
              <div class="w-full h-3 bg-slate-100 rounded-full overflow-hidden">
                <div id="akKpBar" class="h-full bg-indigo-600 rounded-full transition-all duration-300" style="width: 0%"></div>
              </div>
              <p class="text-[11px] text-slate-500" id="akKpNote">Kurang 150,00 AK untuk kenaikan pangkat reguler.</p>
            </div>

            <!-- Progress Kenaikan Jenjang -->
            <div class="space-y-1.5" id="akJenjangProgressBox">
              <div class="flex justify-between text-xs font-semibold">
                <span class="text-slate-700">Target Kenaikan Jenjang Jabatan</span>
                <span id="akKjText" class="text-emerald-700">0 / 450</span>
              </div>
              <div class="w-full h-3 bg-slate-100 rounded-full overflow-hidden">
                <div id="akKjBar" class="h-full bg-emerald-500 rounded-full transition-all duration-300" style="width: 0%"></div>
              </div>
              <p class="text-[11px] text-slate-500" id="akKjNote">Wajib lulus Uji Kompetensi & tersedia lowongan kebutuhan jabatan (Pasal 24).</p>
            </div>

            <!-- Tabel Riwayat Konversi -->
            <div>
              <div class="flex items-center justify-between mb-2">
                <h4 class="text-xs font-bold uppercase tracking-wider text-slate-500">Rincian Perolehan per Periode</h4>
                <button type="button" onclick="clearAkPeriods()" class="text-xs font-semibold text-rose-600 hover:underline">Reset Riwayat</button>
              </div>
              <div class="overflow-x-auto border border-slate-200 rounded-xl">
                <table class="w-full text-left text-xs">
                  <thead class="bg-slate-50 text-slate-600 font-semibold border-b border-slate-200">
                    <tr>
                      <th class="px-3 py-2.5">Tahun/Periode</th>
                      <th class="px-3 py-2.5">Bulan</th>
                      <th class="px-3 py-2.5">Predikat</th>
                      <th class="px-3 py-2.5 text-right">Perolehan AK</th>
                      <th class="px-3 py-2.5 text-center">Aksi</th>
                    </tr>
                  </thead>
                  <tbody id="akTableBody" class="divide-y divide-slate-100">
                    <!-- Diisi JS -->
                  </tbody>
                </table>
              </div>
            </div>
          </div>

          <!-- Tabel Referensi Cepat Lampiran II -->
          <div class="bg-slate-900 text-slate-100 rounded-2xl p-5 shadow-sm">
            <h4 class="text-sm font-bold mb-3">Referensi Konversi Angka Kredit (Lampiran II)</h4>
            <div class="overflow-x-auto">
              <table class="w-full text-xs text-left">
                <thead class="text-slate-400 border-b border-slate-700">
                  <tr>
                    <th class="py-2 pr-3">Jenjang</th>
                    <th class="py-2 px-2 text-right">Koef.</th>
                    <th class="py-2 px-2 text-right">Sangat Baik (150%)</th>
                    <th class="py-2 px-2 text-right">Baik (100%)</th>
                    <th class="py-2 px-2 text-right">Min. KP</th>
                    <th class="py-2 pl-2 text-right">Min. Jenjang</th>
                  </tr>
                </thead>
                <tbody class="divide-y divide-slate-800">
                  <tr>
                    <td class="py-2 pr-3 font-medium">Ahli Muda (III/c-III/d)</td>
                    <td class="py-2 px-2 text-right">25</td>
                    <td class="py-2 px-2 text-right text-emerald-400">37,50</td>
                    <td class="py-2 px-2 text-right">25,00</td>
                    <td class="py-2 px-2 text-right">100</td>
                    <td class="py-2 pl-2 text-right">200</td>
                  </tr>
                  <tr>
                    <td class="py-2 pr-3 font-medium">Ahli Madya (IV/a-IV/c)</td>
                    <td class="py-2 px-2 text-right">37,5</td>
                    <td class="py-2 px-2 text-right text-emerald-400">56,25</td>
                    <td class="py-2 px-2 text-right">37,50</td>
                    <td class="py-2 px-2 text-right">150</td>
                    <td class="py-2 pl-2 text-right">450</td>
                  </tr>
                  <tr>
                    <td class="py-2 pr-3 font-medium">Ahli Utama (IV/d-IV/e)</td>
                    <td class="py-2 px-2 text-right">50</td>
                    <td class="py-2 px-2 text-right text-emerald-400">75,00</td>
                    <td class="py-2 px-2 text-right">50,00</td>
                    <td class="py-2 px-2 text-right">200</td>
                    <td class="py-2 pl-2 text-right">-</td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
        </div>
      </div>
    </section>

  </main>

  <!-- ==================== FOOTER ==================== -->
  <footer class="border-t border-slate-200 bg-white py-4 mt-8 no-print">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col sm:flex-row items-center justify-between gap-2 text-xs text-slate-500">
      <p>SIWAS 28/2026 • Disusun berdasarkan Permendikdasmen Nomor 28 Tahun 2026.</p>
      <p>Aplikasi Kerja Pengawas Sekolah Formal (PAUD, Dikdas, Dikmen).</p>
    </div>
  </footer>

  <!-- ==================== MODAL PROFIL PENGAWAS ==================== -->
  <div id="profileModal" class="fixed inset-0 z-50 hidden items-center justify-center bg-slate-900/50 backdrop-blur-xs p-4 no-print">
    <div class="bg-white rounded-2xl max-w-md w-full p-6 shadow-xl border border-slate-200">
      <div class="flex items-center justify-between mb-4">
        <h3 class="text-base font-bold text-slate-900">Profil Pengawas Sekolah</h3>
        <button type="button" id="btnCloseProfile" class="p-1.5 rounded-lg text-slate-400 hover:bg-slate-100 hover:text-slate-600">
          <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>
      <form id="formProfile" class="space-y-3.5">
        <div>
          <label class="block text-xs font-semibold text-slate-700 mb-1">Nama Lengkap & Gelar</label>
          <input type="text" id="profName" required class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 outline-none focus:ring-2 focus:ring-indigo-500" />
        </div>
        <div>
          <label class="block text-xs font-semibold text-slate-700 mb-1">NIP</label>
          <input type="text" id="profNip" required class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 outline-none focus:ring-2 focus:ring-indigo-500" />
        </div>
        <div class="grid grid-cols-2 gap-3">
          <div>
            <label class="block text-xs font-semibold text-slate-700 mb-1">Jenjang JF</label>
            <select id="profJenjang" class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 bg-white outline-none">
              <option value="muda">Ahli Muda</option>
              <option value="madya">Ahli Madya</option>
              <option value="utama">Ahli Utama</option>
            </select>
          </div>
          <div>
            <label class="block text-xs font-semibold text-slate-700 mb-1">Golongan Ruang</label>
            <select id="profGol" class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 bg-white outline-none">
              <option value="III/c">III/c</option>
              <option value="III/d">III/d</option>
              <option value="IV/a">IV/a</option>
              <option value="IV/b">IV/b</option>
              <option value="IV/c">IV/c</option>
              <option value="IV/d">IV/d</option>
              <option value="IV/e">IV/e</option>
            </select>
          </div>
        </div>
        <div>
          <label class="block text-xs font-semibold text-slate-700 mb-1">Instansi / Dinas Pendidikan</label>
          <input type="text" id="profInstansi" class="w-full px-3 py-2.5 text-sm rounded-xl border border-slate-300 outline-none focus:ring-2 focus:ring-indigo-500" />
        </div>
        <div class="pt-2 flex justify-end gap-2">
          <button type="button" id="btnCancelProfile" class="px-4 py-2.5 rounded-xl text-xs font-semibold text-slate-600 bg-slate-100 hover:bg-slate-200">Batal</button>
          <button type="submit" class="px-4 py-2.5 rounded-xl text-xs font-semibold text-white bg-indigo-600 hover:bg-indigo-700">Simpan Profil</button>
        </div>
      </form>
    </div>
  </div>

  <!-- ==================== MODAL TAHUN PELAJARAN MANUAL ==================== -->
  <div id="tpModal" class="fixed inset-0 z-50 hidden items-center justify-center bg-slate-900/50 backdrop-blur-xs p-4 no-print">
    <div class="bg-white rounded-2xl max-w-sm w-full p-6 shadow-xl border border-slate-200">
      <div class="flex items-center justify-between mb-4">
        <h3 class="text-base font-bold text-slate-900">Atur Tahun Pelajaran</h3>
        <button type="button" id="btnCloseTp" class="p-1.5 rounded-lg text-slate-400 hover:bg-slate-100 hover:text-slate-600">
          <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>
      <form id="formTp" class="space-y-4">
        <div>
          <label for="inputTahunPelajaran" class="block text-xs font-semibold text-slate-700 mb-1.5">Tahun Pelajaran Aktif (Isi Manual)</label>
          <input type="text" id="inputTahunPelajaran" required placeholder="Contoh: 2026/2027 atau 2026/2027 Ganjil" class="w-full px-3.5 py-2.5 text-sm rounded-xl border border-slate-300 outline-none focus:ring-2 focus:ring-indigo-500" />
          <p class="text-[11px] text-slate-500 mt-1.5">Tahun pelajaran ini otomatis melekat pada penilaian 16 indikator, jurnal baru, ekspor CSV, dan kop cetak laporan.</p>
        </div>
        <div class="flex justify-end gap-2">
          <button type="button" id="btnCancelTp" class="px-4 py-2 rounded-xl text-xs font-semibold text-slate-600 bg-slate-100 hover:bg-slate-200">Batal</button>
          <button type="submit" class="px-4 py-2 rounded-xl text-xs font-semibold text-white bg-indigo-600 hover:bg-indigo-700">Simpan</button>
        </div>
      </form>
    </div>
  </div>

  <!-- ==================== MODAL ADMIN TERSEMBUNYI (KELOLA NIP) ==================== -->
  <div id="adminModal" class="fixed inset-0 z-50 hidden items-center justify-center bg-slate-900/60 backdrop-blur-xs p-4 no-print">
    <div class="bg-white rounded-2xl max-w-2xl w-full max-h-[90vh] flex flex-col shadow-2xl border border-slate-200 overflow-hidden">
      <!-- Header Modal Admin -->
      <div class="p-5 border-b border-slate-200 flex items-center justify-between bg-slate-900 text-white">
        <div class="flex items-center gap-2.5">
          <span class="px-2.5 py-1 rounded-lg bg-amber-500/20 text-amber-300 text-xs font-bold border border-amber-400/30">ADMIN</span>
          <div>
            <h3 class="text-sm sm:text-base font-bold">Pengaturan NIP Pengawas Sekolah</h3>
            <p class="text-[11px] text-slate-400">Kelola daftar NIP yang diizinkan masuk ke SIWAS 28/2026</p>
          </div>
        </div>
        <button type="button" id="btnCloseAdmin" class="p-1.5 rounded-lg text-slate-400 hover:bg-slate-800 hover:text-white transition">
          <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>

      <!-- Konten Modal Admin -->
      <div class="p-5 overflow-y-auto space-y-5">
        <!-- Form Tambah NIP Pengawas -->
        <form id="formAdminAddUser" class="bg-slate-50 rounded-xl p-4 border border-slate-200 space-y-3">
          <h4 class="text-xs font-bold uppercase tracking-wider text-slate-600">Tambah Akun Pengawas Baru</h4>
          <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
            <div>
              <label class="block text-xs font-semibold text-slate-700 mb-1">NIP Pengawas</label>
              <input type="text" id="admNip" required placeholder="19xxxxxxxxxxxxxx" class="w-full px-3 py-2 text-xs sm:text-sm rounded-lg border border-slate-300 bg-white outline-none focus:ring-2 focus:ring-indigo-500" />
            </div>
            <div>
              <label class="block text-xs font-semibold text-slate-700 mb-1">Nama Lengkap & Gelar</label>
              <input type="text" id="admName" required placeholder="Nama Pengawas, M.Pd." class="w-full px-3 py-2 text-xs sm:text-sm rounded-lg border border-slate-300 bg-white outline-none focus:ring-2 focus:ring-indigo-500" />
            </div>
          </div>
          <div class="grid grid-cols-1 sm:grid-cols-3 gap-3">
            <div>
              <label class="block text-xs font-semibold text-slate-700 mb-1">Jenjang JF</label>
              <select id="admJenjang" class="w-full px-3 py-2 text-xs sm:text-sm rounded-lg border border-slate-300 bg-white outline-none">
                <option value="muda">Ahli Muda</option>
                <option value="madya" selected>Ahli Madya</option>
                <option value="utama">Ahli Utama</option>
              </select>
            </div>
            <div>
              <label class="block text-xs font-semibold text-slate-700 mb-1">Golongan</label>
              <select id="admGol" class="w-full px-3 py-2 text-xs sm:text-sm rounded-lg border border-slate-300 bg-white outline-none">
                <option value="III/c">III/c</option>
                <option value="III/d">III/d</option>
                <option value="IV/a" selected>IV/a</option>
                <option value="IV/b">IV/b</option>
                <option value="IV/c">IV/c</option>
                <option value="IV/d">IV/d</option>
                <option value="IV/e">IV/e</option>
              </select>
            </div>
            <div>
              <label class="block text-xs font-semibold text-slate-700 mb-1">Instansi</label>
              <input type="text" id="admInstansi" value="Dinas Pendidikan" class="w-full px-3 py-2 text-xs sm:text-sm rounded-lg border border-slate-300 bg-white outline-none focus:ring-2 focus:ring-indigo-500" />
            </div>
          </div>
          <div id="adminFormError" class="hidden text-xs text-rose-600 font-medium"></div>
          <button type="submit" class="w-full sm:w-auto px-4 py-2 rounded-lg bg-indigo-600 hover:bg-indigo-700 text-white text-xs font-semibold transition">
            + Daftarkan NIP Pengawas
          </button>
        </form>

        <!-- Daftar NIP Terdaftar -->
        <div>
          <div class="flex items-center justify-between mb-2">
            <h4 class="text-xs font-bold uppercase tracking-wider text-slate-600">Daftar NIP Pengawas Terdaftar</h4>
            <span id="adminUserCount" class="text-xs font-semibold text-indigo-600">0 Akun</span>
          </div>
          <div class="border border-slate-200 rounded-xl overflow-x-auto">
            <table class="w-full text-left text-xs">
              <thead class="bg-slate-50 text-slate-600 font-semibold border-b border-slate-200">
                <tr>
                  <th class="px-3 py-2.5">NIP</th>
                  <th class="px-3 py-2.5">Nama & Instansi</th>
                  <th class="px-3 py-2.5">Jenjang / Gol</th>
                  <th class="px-3 py-2.5 text-center">Aksi</th>
                </tr>
              </thead>
              <tbody id="adminUserTableBody" class="divide-y divide-slate-100">
                <!-- Diisi dinamis oleh JS -->
              </tbody>
            </table>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- ==================== TOAST NOTIFICATION ==================== -->
  <div id="toast" class="fixed bottom-5 right-5 z-50 hidden items-center gap-2.5 px-4 py-3 rounded-xl bg-slate-900 text-white text-xs sm:text-sm font-medium shadow-lg no-print">
    <span class="w-2 h-2 rounded-full bg-emerald-400"></span>
    <span id="toastMessage">Berhasil disimpan</span>
  </div>

  <!-- ==================== JAVASCRIPT LOGIC ==================== -->
  <script>
    /**
     * DATA RESMI TUPOKSI PENGAWAS SEKOLAH
     * Sumber: Lampiran I Bagian C Permendikdasmen Nomor 28 Tahun 2026 (Halaman 96-102)
     */
    const TUPOKSI_DATA = {
      muda: {
        label: 'Pengawas Sekolah Ahli Muda',
        golongan: 'III/c - III/d',
        fokus: 'Melakukan analisis mutu melalui pengawasan manajerial dan akademik pada Satuan Pendidikan formal.',
        koefisien: 25,
        minKP: 100,
        minKJ: 200,
        pillars: {
          pemantauan: {
            title: '1. Melaksanakan pemantauan sebagai acuan analisis mutu',
            items: [
              'a. Pemantauan perencanaan program Satuan Pendidikan untuk memperoleh data sebagai acuan analisis mutu aspek manajerial.',
              'b. Pemantauan pelaksanaan Standar Nasional Pendidikan (SNP) di Satuan Pendidikan binaan sebagai acuan analisis mutu manajerial.',
              'c. Pemantauan capaian mutu Satuan Pendidikan binaan, termasuk implementasi budaya dan nilai karakter dalam tata kelola.',
              'd. Pemantauan praktik pengembangan keprofesian berkelanjutan (PKB) bagi Guru dan Kepala Sekolah sebagai dasar analisis mutu.',
              'e. Pemantauan peningkatan capaian Rapor Pendidikan dengan menganalisis mutu literasi, numerasi, dan karakter siswa.'
            ]
          },
          penilaian: {
            title: '2. Melaksanakan penilaian sebagai acuan analisis mutu',
            items: [
              'a. Penilaian perencanaan program Satuan Pendidikan sebagai dasar analisis mutu aspek manajerial.',
              'b. Penilaian keterlaksanaan pengelolaan Satuan Pendidikan berdasarkan SNP sebagai dasar analisis mutu.',
              'c. Penilaian dan pemberian rekomendasi kinerja Kepala Sekolah dalam pengelolaan Satuan Pendidikan termasuk budaya dan nilai karakter.',
              'd. Penilaian keterlaksanaan pembelajaran berdasarkan standar sebagai dasar analisis mutu pembelajaran.',
              'e. Penilaian implementasi program pengembangan profesi Kepala Sekolah dan Guru sebagai acuan analisis mutu.',
              'f. Penilaian efektivitas supervisi akademik oleh Kepala Sekolah untuk pengembangan mutu pembelajaran dan kompetensi Guru.'
            ]
          },
          pembinaan: {
            title: '3. Melaksanakan pembinaan manajerial dan akademik dalam lingkup analisis mutu',
            items: [
              'a. Pembinaan manajerial perbaikan pengelolaan dan pemenuhan SNP kepada Kepala Sekolah dan tenaga kependidikan.',
              'b. Pembinaan manajerial penyusunan & pelaksanaan RTL peningkatan mutu, penguatan kepemimpinan dan budaya berbasis karakter kepada Kepala Sekolah.',
              'c. Pembinaan akademik peningkatan kompetensi metode pembelajaran yang berkesadaran, bermakna, dan menggembirakan serta penilaian sesuai SNP untuk literasi, numerasi, dan karakter kepada Guru.',
              'd. Pembinaan pelaksanaan PKB bagi Guru melalui komunitas belajar di Satuan Pendidikan dalam lingkup analisis mutu.',
              'e. Pembinaan akademik terkait refleksi dan tindak lanjut peningkatan kualitas pembelajaran bagi Guru.'
            ]
          }
        }
      },
      madya: {
        label: 'Pengawas Sekolah Ahli Madya',
        golongan: 'IV/a - IV/b - IV/c',
        fokus: 'Melakukan pengendalian dan pengembangan mutu melalui pengawasan manajerial dan akademik pada Satuan Pendidikan formal.',
        koefisien: 37.5,
        minKP: 150,
        minKJ: 450,
        pillars: {
          pemantauan: {
            title: '1. Melaksanakan pemantauan sebagai acuan pengendalian dan pengembangan mutu',
            items: [
              'a. Pemantauan perencanaan program Satuan Pendidikan sebagai acuan pengendalian dan pengembangan mutu aspek manajerial.',
              'b. Pemantauan pelaksanaan SNP di Satuan Pendidikan binaan sebagai acuan pengendalian dan pengembangan mutu manajerial.',
              'c. Pemantauan capaian mutu Satuan Pendidikan binaan, termasuk implementasi budaya dan nilai karakter dalam tata kelola.',
              'd. Pemantauan praktik pengembangan keprofesian Guru dan Kepala Sekolah sebagai dasar pengendalian dan pengembangan mutu.',
              'e. Pemantauan peningkatan capaian Rapor Pendidikan dengan menganalisis mutu literasi, numerasi, dan karakter siswa.'
            ]
          },
          penilaian: {
            title: '2. Melaksanakan penilaian sebagai acuan pengendalian dan pengembangan mutu',
            items: [
              'a. Penilaian perencanaan program Satuan Pendidikan sebagai dasar pengendalian dan pengembangan mutu manajerial.',
              'b. Penilaian keterlaksanaan pengelolaan Satuan Pendidikan berdasarkan SNP sebagai dasar pengendalian dan pengembangan mutu.',
              'c. Penilaian dan pemberian rekomendasi kinerja Kepala Sekolah dalam pengelolaan Satuan Pendidikan termasuk budaya dan nilai karakter.',
              'd. Penilaian keterlaksanaan pembelajaran berdasarkan standar untuk pengendalian dan pengembangan mutu pembelajaran.',
              'e. Penilaian implementasi program pengembangan profesi bagi Kepala Sekolah dan Guru sebagai acuan pengendalian dan pengembangan mutu.',
              'f. Evaluasi efektivitas supervisi akademik oleh Kepala Sekolah sebagai acuan pengendalian dan pengembangan mutu pembelajaran.'
            ]
          },
          pembinaan: {
            title: '3. Melaksanakan pembinaan manajerial dan akademik dalam lingkup pengendalian dan pengembangan mutu',
            items: [
              'a. Pembinaan manajerial perbaikan pengelolaan dan pemenuhan SNP berdasarkan hasil penilaian kepada Kepala Sekolah dan tendik.',
              'b. Pembinaan manajerial penyusunan & pelaksanaan RTL peningkatan mutu, penguatan kepemimpinan dan budaya berbasis karakter kepada Kepala Sekolah.',
              'c. Pembinaan akademik metode pembelajaran berkesadaran, bermakna, dan menggembirakan serta penilaian sesuai SNP untuk literasi, numerasi, dan karakter kepada Guru.',
              'd. Pembinaan pelaksanaan PKB bagi Guru melalui kolaborasi lintas Satuan Pendidikan dengan sumber daya dan strategi sesuai.',
              'e. Pembinaan akademik terkait refleksi dan tindak lanjut peningkatan kualitas pembelajaran bagi Guru.'
            ]
          }
        }
      },
      utama: {
        label: 'Pengawas Sekolah Ahli Utama',
        golongan: 'IV/d - IV/e',
        fokus: 'Melakukan kegiatan strategis dan inovasi pengembangan sistem pengawasan manajerial dan akademik pada Satuan Pendidikan formal.',
        koefisien: 50,
        minKP: 200,
        minKJ: null,
        pillars: {
          pemantauan: {
            title: '1. Melaksanakan pemantauan sebagai acuan pengembangan sistem yang strategis dan inovatif',
            items: [
              'a. Pemantauan perencanaan program Satuan Pendidikan sebagai acuan pengembangan sistem strategis dan inovatif aspek manajerial.',
              'b. Pemantauan pelaksanaan SNP di Satuan Pendidikan binaan sebagai acuan kegiatan strategis dan inovasi pengembangan sistem.',
              'c. Pemantauan data capaian mutu termasuk budaya dan nilai karakter dalam tata kelola sebagai acuan inovasi pengembangan sistem.',
              'd. Pemantauan praktik pengembangan profesional Guru dan Kepala Sekolah sebagai dasar pengembangan sistem strategis dan inovatif.',
              'e. Pemantauan peningkatan capaian Rapor Pendidikan (literasi, numerasi, karakter) dalam rangka kegiatan strategis dan inovasi sistem.'
            ]
          },
          penilaian: {
            title: '2. Melaksanakan penilaian sebagai acuan pengembangan sistem yang strategis dan inovatif',
            items: [
              'a. Penilaian perencanaan program Satuan Pendidikan sebagai dasar penyusunan kegiatan strategis pengembangan sistem inovatif.',
              'b. Penilaian keterlaksanaan pengelolaan Satuan Pendidikan berdasarkan SNP sebagai dasar sistem pengawasan strategis & inovatif.',
              'c. Penilaian dan pemberian rekomendasi kinerja Kepala Sekolah termasuk budaya dan nilai karakter dalam manajemen sekolah.',
              'd. Penilaian keterlaksanaan pembelajaran berdasarkan SNP sebagai acuan dalam mengembangkan inovasi pembelajaran.',
              'e. Penilaian implementasi program pengembangan profesi KS dan Guru sebagai dasar penyusunan rencana strategis kompetensi.',
              'f. Evaluasi efektivitas supervisi akademik oleh Kepala Sekolah sebagai acuan pengembangan inovasi peningkatan kompetensi.'
            ]
          },
          pembinaan: {
            title: '3. Melaksanakan pembinaan manajerial dan akademik dalam lingkup inovasi pengembangan sistem',
            items: [
              'a. Pembinaan manajerial perbaikan pengelolaan dan SNP dalam lingkup inovasi pengembangan sistem kepada Kepala Sekolah & tendik.',
              'b. Pembinaan manajerial penyusunan & pelaksanaan RTL peningkatan mutu, penguatan kepemimpinan dan budaya karakter dalam lingkup inovasi sistem.',
              'c. Pembinaan akademik metode pembelajaran berkesadaran, bermakna, menggembirakan serta penilaian SNP untuk literasi, numerasi, dan karakter sebagai acuan inovasi sistem.',
              'd. Pembinaan pelaksanaan PKB bagi Guru melalui jejaring kolaborasi lintas wilayah/instansi dalam lingkup inovasi dan pengembangan sistem.',
              'e. Pembinaan akademik terkait refleksi dan tindak lanjut dalam pengembangan strategi pembelajaran yang inovatif.'
            ]
          }
        }
      }
    };

    // Rubrik Skor Indikator 1 - 4 beserta keterangannya
    const SCORE_RUBRIC = {
      1: {
        label: 'Kurang',
        desc: 'Belum memenuhi standar; perlu pembinaan intensif.',
        badge: 'bg-rose-100 text-rose-700 border-rose-200',
        activeBtn: 'bg-rose-600 text-white border-rose-600 shadow-xs'
      },
      2: {
        label: 'Cukup',
        desc: 'Sebagian terpenuhi; perlu perbaikan terarah.',
        badge: 'bg-amber-100 text-amber-700 border-amber-200',
        activeBtn: 'bg-amber-500 text-white border-amber-500 shadow-xs'
      },
      3: {
        label: 'Baik',
        desc: 'Memenuhi Standar Nasional Pendidikan (SNP).',
        badge: 'bg-blue-100 text-blue-700 border-blue-200',
        activeBtn: 'bg-blue-600 text-white border-blue-600 shadow-xs'
      },
      4: {
        label: 'Sangat Baik',
        desc: 'Melampaui standar, konsisten & inovatif.',
        badge: 'bg-emerald-100 text-emerald-700 border-emerald-200',
        activeBtn: 'bg-emerald-600 text-white border-emerald-600 shadow-xs'
      }
    };

    // ==================== STATE APLIKASI (IN-MEMORY + SAFE SESSION) ====================
    let currentSessionNip = null;

    let appState = {
      tahunPelajaran: '2026/2027',
      registeredUsers: [
        {
          nip: '197205141998021001',
          name: 'Drs. Budi Santoso, M.Pd.',
          jenjang: 'madya',
          gol: 'IV/a',
          instansi: 'Dinas Pendidikan dan Kebudayaan'
        },
        {
          nip: '197808172005012004',
          name: 'Dra. Sri Wahyuni, M.Pd.',
          jenjang: 'muda',
          gol: 'III/d',
          instansi: 'Dinas Pendidikan dan Kebudayaan'
        }
      ],
      profile: {
        name: 'Drs. Budi Santoso, M.Pd.',
        nip: '197205141998021001',
        jenjang: 'madya',
        gol: 'IV/a',
        instansi: 'Dinas Pendidikan dan Kebudayaan'
      },
      schools: [
        { id: 'sch-1', name: 'SDN 1 Harapan Bangsa', level: 'SD', npsn: '20310001', principal: 'Siti Aminah, S.Pd.', priority: 'Penguatan Literasi & Numerasi' },
        { id: 'sch-2', name: 'SMPN 2 Nusantara', level: 'SMP', npsn: '20310045', principal: 'Ahmad Fauzi, M.Pd.', priority: 'Peningkatan Kualitas Pembelajaran' }
      ],
      // Menyimpan skor (1-4) dan bukti dukung untuk setiap indikator (16 butir)
      // Key: `${tahunPelajaran}||${schoolName}||${jenjang}||${pillar}||${idx}`
      indicatorAssessments: {
        '2026/2027||SDN 1 Harapan Bangsa||madya||pemantauan||4': {
          score: 3,
          evidence: 'Rekap Rapor Pendidikan 2026 & Berita Acara Pemantauan.pdf'
        }
      },
      logs: [
        {
          id: 'log-1',
          date: new Date().toISOString().split('T')[0],
          tahunPelajaran: '2026/2027',
          schoolName: 'SDN 1 Harapan Bangsa',
          pillar: 'pemantauan',
          indicator: 'e. Pemantauan peningkatan capaian Rapor Pendidikan dengan menganalisis mutu literasi, numerasi, dan karakter siswa.',
          score: 3,
          finding: 'Capaian numerasi kelas V masih berada pada kategori sedang; pemanfaatan buku nonteks di pojok baca perlu dioptimalkan.',
          rtl: 'Menyusun jadwal pendampingan komunitas belajar guru kelas atas untuk perancangan pembelajaran numerasi kontekstual.',
          evidence: 'Berita Acara Pemantauan & Rekap Rapor Pendidikan 2026.pdf',
          status: 'Terlaksana'
        }
      ],
      akPeriods: [
        { id: 'ak-1', label: '2025', months: 12, predikatVal: 1.0, predikatLabel: 'Baik (100%)' },
        { id: 'ak-2', label: '2026', months: 12, predikatVal: 1.5, predikatLabel: 'Sangat Baik (150%)' }
      ]
    };

    let currentAnalysisJenjang = 'madya';
    let currentPillarFilter = 'all';

    // ==================== AUTH & ADMIN TERSEMBUNYI (KLIK LOGO 3X) ====================
    function setupTripleClick(elementId, onTripleClick) {
      const el = document.getElementById(elementId);
      if (!el) return;
      let clickCount = 0;
      let clickTimer = null;

      el.addEventListener('click', () => {
        clickCount += 1;
        clearTimeout(clickTimer);
        if (clickCount >= 3) {
          clickCount = 0;
          onTripleClick();
        } else {
          clickTimer = setTimeout(() => {
            clickCount = 0;
          }, 1200);
        }
      });
    }

    function checkAuthState() {
      const overlay = document.getElementById('loginOverlay');
      if (!currentSessionNip) {
        overlay.classList.remove('hidden');
        overlay.classList.add('flex');
        return false;
      }
      const user = appState.registeredUsers.find(u => u.nip === currentSessionNip);
      if (!user) {
        currentSessionNip = null;
        overlay.classList.remove('hidden');
        overlay.classList.add('flex');
        return false;
      }
      appState.profile = { ...user };
      overlay.classList.add('hidden');
      overlay.classList.remove('flex');
      return true;
    }

    function handleLogin(e) {
      e.preventDefault();
      const inputNip = document.getElementById('loginNipInput').value.trim();
      const errBox = document.getElementById('loginErrorBox');
      const found = appState.registeredUsers.find(u => u.nip === inputNip);

      if (!found) {
        errBox.classList.remove('hidden');
        return;
      }

      errBox.classList.add('hidden');
      currentSessionNip = found.nip;
      appState.profile = { ...found };

      renderProfile();
      document.getElementById('akJenjang').value = appState.profile.jenjang;
      selectAnalysisJenjang(appState.profile.jenjang || 'madya');
      renderAkCalculator();
      checkAuthState();
      document.getElementById('loginNipInput').value = '';
      showToast(`Selamat datang, ${found.name}`);
    }

    function handleLogout() {
      currentSessionNip = null;
      checkAuthState();
      showToast('Anda telah keluar dari sesi.');
    }

    function openAdminModal() {
      renderAdminUsers();
      const modal = document.getElementById('adminModal');
      modal.classList.remove('hidden');
      modal.classList.add('flex');
      showToast('Panel Admin Terbuka (Klik Logo 3x)');
    }

    function closeAdminModal() {
      const modal = document.getElementById('adminModal');
      modal.classList.add('hidden');
      modal.classList.remove('flex');
    }

    function renderAdminUsers() {
      const tbody = document.getElementById('adminUserTableBody');
      document.getElementById('adminUserCount').textContent = `${appState.registeredUsers.length} Akun`;

      tbody.innerHTML = appState.registeredUsers.map(u => {
        const jLabel = u.jenjang === 'muda' ? 'Ahli Muda' : u.jenjang === 'madya' ? 'Ahli Madya' : 'Ahli Utama';
        return `
          <tr class="hover:bg-slate-50">
            <td class="px-3 py-2.5 font-mono font-semibold text-indigo-700 select-all">${escapeHtml(u.nip)}</td>
            <td class="px-3 py-2.5">
              <p class="font-semibold text-slate-800">${escapeHtml(u.name)}</p>
              <p class="text-[11px] text-slate-500">${escapeHtml(u.instansi || '-')}</p>
            </td>
            <td class="px-3 py-2.5 text-slate-600">${jLabel} (${escapeHtml(u.gol)})</td>
            <td class="px-3 py-2.5 text-center">
              <button type="button" onclick="deleteAdminUser('${escapeHtml(u.nip)}')" class="px-2 py-1 rounded-md text-rose-600 hover:bg-rose-50 font-semibold transition">
                Hapus
              </button>
            </td>
          </tr>
        `;
      }).join('');
    }

    function deleteAdminUser(nip) {
      if (appState.registeredUsers.length <= 1) {
        showToast('Minimal harus ada 1 NIP pengawas terdaftar.');
        return;
      }
      appState.registeredUsers = appState.registeredUsers.filter(u => u.nip !== nip);
      renderAdminUsers();
      if (currentSessionNip === nip) {
        handleLogout();
      } else {
        showToast(`NIP ${nip} berhasil dihapus.`);
      }
    }

    // ==================== TOAST HELPER ====================
    let toastTimer = null;
    function showToast(msg) {
      const toast = document.getElementById('toast');
      document.getElementById('toastMessage').textContent = msg;
      toast.classList.remove('hidden');
      toast.classList.add('flex');
      clearTimeout(toastTimer);
      toastTimer = setTimeout(() => {
        toast.classList.add('hidden');
        toast.classList.remove('flex');
      }, 2800);
    }

    // ==================== TAB NAVIGATION ====================
    function switchTab(tabId) {
      document.querySelectorAll('.tab-panel').forEach(p => p.classList.add('hidden'));
      const target = document.getElementById('tab-' + tabId);
      if (target) target.classList.remove('hidden');

      document.querySelectorAll('.nav-tab').forEach(btn => {
        if (btn.dataset.tab === tabId) {
          btn.className = 'nav-tab flex items-center gap-2 px-4 py-2.5 rounded-xl text-sm font-semibold whitespace-nowrap transition bg-indigo-600 text-white shadow-sm';
        } else {
          btn.className = 'nav-tab flex items-center gap-2 px-4 py-2.5 rounded-xl text-sm font-semibold whitespace-nowrap transition text-slate-600 hover:bg-slate-100';
        }
      });
    }

    // ==================== RENDER PROFIL & TAHUN PELAJARAN ====================
    function renderProfile() {
      const p = appState.profile;
      const jenjangText = p.jenjang === 'muda' ? 'Ahli Muda' : p.jenjang === 'madya' ? 'Ahli Madya' : 'Ahli Utama';
      const initials = p.name.split(' ').slice(0, 2).map(w => w[0] || '').join('').toUpperCase() || 'PS';

      document.getElementById('headerAvatar').textContent = initials;
      document.getElementById('headerName').textContent = p.name;
      document.getElementById('headerRank').textContent = `${jenjangText} (${p.gol})`;

      document.getElementById('printName').textContent = p.name;
      document.getElementById('printNip').textContent = p.nip || '-';
      document.getElementById('printRank').textContent = `Pengawas Sekolah ${jenjangText} / ${p.gol}`;
      document.getElementById('printInstansi').textContent = p.instansi || '-';

      populateIndicatorSelect();
    }

    function renderTahunPelajaran() {
      const tp = appState.tahunPelajaran || '2026/2027';
      document.getElementById('headerTpLabel').textContent = tp;
      document.getElementById('printTp').textContent = tp;
      renderTupoksiList();
    }

    // ==================== TAB 1: ANALISIS TUPOKSI & PENILAIAN 16 INDIKATOR ====================
    function getAssessmentKey(pillar, idx) {
      const tp = appState.tahunPelajaran || '2026/2027';
      const schoolEl = document.getElementById('instrumenSchoolSelect');
      const schoolName = schoolEl ? schoolEl.value : (appState.schools[0]?.name || 'Sekolah Binaan Umum');
      return `${tp}||${schoolName}||${currentAnalysisJenjang}||${pillar}||${idx}`;
    }

    function setIndicatorScore(pillar, idx, scoreVal) {
      const key = getAssessmentKey(pillar, idx);
      const current = appState.indicatorAssessments[key] || { score: null, evidence: '' };
      appState.indicatorAssessments[key] = { ...current, score: scoreVal };
      renderTupoksiList();
    }

    function setIndicatorEvidence(pillar, idx, val) {
      const key = getAssessmentKey(pillar, idx);
      const current = appState.indicatorAssessments[key] || { score: null, evidence: '' };
      appState.indicatorAssessments[key] = { ...current, evidence: val };
      updateEvidenceLinkPreview(pillar, idx, val);
    }

    function updateEvidenceLinkPreview(pillar, idx, val) {
      const previewEl = document.getElementById(`ev-preview-${pillar}-${idx}`);
      if (!previewEl) return;
      const trimmed = (val || '').trim();
      if (/^https?:\/\//i.test(trimmed)) {
        previewEl.innerHTML = `<a href="${escapeHtml(trimmed)}" target="_blank" rel="noopener noreferrer" class="text-[11px] text-indigo-600 hover:underline font-medium inline-flex items-center gap-1 mt-1">Buka tautan bukti dukung ↗</a>`;
      } else {
        previewEl.innerHTML = '';
      }
    }

    function selectAnalysisJenjang(jenjang) {
      currentAnalysisJenjang = jenjang;
      ['muda', 'madya', 'utama'].forEach(j => {
        const card = document.getElementById('card-jenjang-' + j);
        if (!card) return;
        if (j === jenjang) {
          card.classList.add('ring-2', 'ring-inset', 'ring-indigo-600', 'bg-indigo-50/40');
        } else {
          card.classList.remove('ring-2', 'ring-inset', 'ring-indigo-600', 'bg-indigo-50/40');
        }
      });
      renderTupoksiList();
    }

    function setPillarFilter(pillar) {
      currentPillarFilter = pillar;
      document.querySelectorAll('.pillar-btn').forEach(btn => {
        if (btn.dataset.pillar === pillar) {
          btn.className = 'pillar-btn px-3 py-1.5 rounded-lg text-xs font-semibold bg-slate-900 text-white';
        } else {
          btn.className = 'pillar-btn px-3 py-1.5 rounded-lg text-xs font-semibold bg-slate-100 text-slate-600 hover:bg-slate-200';
        }
      });
      renderTupoksiList();
    }

    function updateInstrumenSummary() {
      const data = TUPOKSI_DATA[currentAnalysisJenjang];
      const schoolEl = document.getElementById('instrumenSchoolSelect');
      const schoolName = schoolEl ? schoolEl.value : '-';
      document.getElementById('instrumenSummarySchool').textContent = schoolName;
      document.getElementById('instrumenSummaryTp').textContent = `TP ${appState.tahunPelajaran || '2026/2027'}`;

      let totalScore = 0;
      let filledCount = 0;
      ['pemantauan', 'penilaian', 'pembinaan'].forEach(pKey => {
        data.pillars[pKey].items.forEach((_, idx) => {
          const rec = appState.indicatorAssessments[getAssessmentKey(pKey, idx)];
          if (rec && rec.score) {
            totalScore += Number(rec.score);
            filledCount += 1;
          }
        });
      });

      document.getElementById('instrumenCountFilled').textContent = filledCount;
      const avg = filledCount > 0 ? (totalScore / filledCount) : 0;
      document.getElementById('instrumenAvgScore').textContent = formatNum(avg);

      const badgeBox = document.getElementById('instrumenPredikatBadge');
      if (filledCount === 0) {
        badgeBox.innerHTML = `<span class="px-2.5 py-1 rounded-lg text-xs font-bold bg-slate-200 text-slate-600">Belum Dinilai</span>`;
      } else {
        const rounded = Math.min(4, Math.max(1, Math.round(avg)));
        const rub = SCORE_RUBRIC[rounded];
        badgeBox.innerHTML = `<span class="px-2.5 py-1 rounded-lg text-xs font-bold border ${rub.badge}">${rub.label}</span>`;
      }
    }

    function renderTupoksiList() {
      const data = TUPOKSI_DATA[currentAnalysisJenjang];
      document.getElementById('analysisTitle').textContent = `Instrumen 16 Indikator: ${data.label}`;
      document.getElementById('analysisSubtitle').textContent = `Fokus: ${data.fokus}`;

      const container = document.getElementById('tupoksiListContainer');
      container.innerHTML = '';

      const pillarKeys = currentPillarFilter === 'all' ? ['pemantauan', 'penilaian', 'pembinaan'] : [currentPillarFilter];
      const badgeStyles = {
        pemantauan: { bg: 'bg-blue-50/70 border-blue-200', title: 'text-blue-800', dot: 'bg-blue-500' },
        penilaian: { bg: 'bg-amber-50/70 border-amber-200', title: 'text-amber-800', dot: 'bg-amber-500' },
        pembinaan: { bg: 'bg-emerald-50/70 border-emerald-200', title: 'text-emerald-800', dot: 'bg-emerald-500' }
      };

      pillarKeys.forEach(pKey => {
        const pillar = data.pillars[pKey];
        const st = badgeStyles[pKey];
        const block = document.createElement('div');
        block.className = `rounded-2xl border ${st.bg} p-4 sm:p-5 space-y-3`;

        const itemsHtml = pillar.items.map((item, idx) => {
          const rec = appState.indicatorAssessments[getAssessmentKey(pKey, idx)] || { score: null, evidence: '' };
          const activeRubric = rec.score ? SCORE_RUBRIC[rec.score] : null;
          const evTrim = (rec.evidence || '').trim();
          const isUrl = /^https?:\/\//i.test(evTrim);

          const scoreButtonsHtml = [1, 2, 3, 4].map(n => {
            const isSelected = Number(rec.score) === n;
            const r = SCORE_RUBRIC[n];
            const btnClass = isSelected
              ? r.activeBtn
              : 'bg-white text-slate-700 border-slate-200 hover:bg-slate-100';
            return `
              <button type="button" onclick="setIndicatorScore('${pKey}', ${idx}, ${n})" title="${r.label}: ${r.desc}" class="px-2.5 py-1.5 rounded-lg border text-xs font-bold transition ${btnClass}">
                ${n} • ${r.label}
              </button>
            `;
          }).join('');

          return `
            <div class="print-card bg-white rounded-xl p-4 border border-slate-200/80 shadow-2xs space-y-3">
              <!-- Teks Indikator -->
              <p class="text-xs sm:text-sm font-medium text-slate-800 leading-relaxed">${escapeHtml(item)}</p>

              <!-- Baris Skor 1,2,3,4 + Keterangan & Kolom Bukti Dukung -->
              <div class="grid grid-cols-1 lg:grid-cols-12 gap-3 pt-2 border-t border-slate-100 items-start">
                <!-- Skor 1-4 beserta Keterangan -->
                <div class="lg:col-span-7 space-y-2">
                  <div class="flex flex-wrap items-center gap-1.5">
                    <span class="text-[11px] font-semibold text-slate-500 mr-1">Skor:</span>
                    ${scoreButtonsHtml}
                  </div>
                  <div class="text-[11px] px-2.5 py-1.5 rounded-lg ${activeRubric ? activeRubric.badge + ' border' : 'bg-slate-50 text-slate-500 border border-slate-200'}">
                    ${activeRubric
                      ? `<strong>Skor ${rec.score} (${activeRubric.label}):</strong> ${activeRubric.desc}`
                      : '<em>Belum dipilih.</em> (1: Kurang | 2: Cukup | 3: Baik / Memenuhi SNP | 4: Sangat Baik / Inovatif)'}
                  </div>
                </div>

                <!-- Kolom Bukti Dukung -->
                <div class="lg:col-span-5">
                  <label class="block text-[11px] font-semibold text-slate-500 mb-1">Bukti Dukung (Dokumen / Link URL)</label>
                  <input
                    type="text"
                    value="${escapeHtml(rec.evidence || '')}"
                    oninput="setIndicatorEvidence('${pKey}', ${idx}, this.value)"
                    placeholder="Nama dokumen atau https://drive.google.com/..."
                    class="w-full px-3 py-2 text-xs rounded-lg border border-slate-300 focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 outline-none"
                  />
                  <div id="ev-preview-${pKey}-${idx}">
                    ${isUrl ? `<a href="${escapeHtml(evTrim)}" target="_blank" rel="noopener noreferrer" class="text-[11px] text-indigo-600 hover:underline font-medium inline-flex items-center gap-1 mt-1">Buka tautan bukti dukung ↗</a>` : ''}
                  </div>
                </div>
              </div>
            </div>
          `;
        }).join('');

        block.innerHTML = `
          <h4 class="font-bold text-sm ${st.title} flex items-center gap-2">
            <span class="w-2.5 h-2.5 rounded-full ${st.dot}"></span>
            ${pillar.title}
          </h4>
          <div class="space-y-3">
            ${itemsHtml}
          </div>
        `;
        container.appendChild(block);
      });

      updateInstrumenSummary();
    }

    function exportInstrumenCSV() {
      const data = TUPOKSI_DATA[currentAnalysisJenjang];
      const tp = appState.tahunPelajaran || '2026/2027';
      const schoolEl = document.getElementById('instrumenSchoolSelect');
      const schoolName = schoolEl ? schoolEl.value : '-';

      const headers = ['Tahun Pelajaran', 'Sekolah Binaan', 'Jenjang Pengawas', 'Pilar', 'Indikator Cakupan Kegiatan', 'Skor (1-4)', 'Predikat', 'Keterangan Skor', 'Bukti Dukung'];
      const rows = [];

      ['pemantauan', 'penilaian', 'pembinaan'].forEach(pKey => {
        data.pillars[pKey].items.forEach((item, idx) => {
          const rec = appState.indicatorAssessments[getAssessmentKey(pKey, idx)] || { score: '', evidence: '' };
          const rub = rec.score ? SCORE_RUBRIC[rec.score] : null;
          rows.push([
            tp,
            schoolName,
            data.label,
            pKey.toUpperCase(),
            item,
            rec.score || '-',
            rub ? rub.label : 'Belum Dinilai',
            rub ? rub.desc : '-',
            rec.evidence || '-'
          ].map(v => `"${String(v).replace(/"/g, '""')}"`).join(','));
        });
      });

      const csv = [headers.join(','), ...rows].join('\n');
      const blob = new Blob([csv], { type: 'text/csv;charset=utf-8;' });
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url;
      a.download = `Instrumen_16_Indikator_${schoolName.replace(/\s+/g, '_')}.csv`;
      a.click();
      URL.revokeObjectURL(url);
      showToast('CSV Instrumen 16 Indikator berhasil diunduh.');
    }

    // ==================== TAB 2: JURNAL PENGAWASAN ====================
    function populateSchoolSelect() {
      const optionsHtml = appState.schools.length === 0
        ? '<option value="Sekolah Binaan Umum">Sekolah Binaan Umum</option>'
        : appState.schools.map(s => `<option value="${escapeHtml(s.name)}">${escapeHtml(s.name)} (${s.level})</option>`).join('');

      const logSel = document.getElementById('logSchool');
      if (logSel) logSel.innerHTML = optionsHtml;

      const instrSel = document.getElementById('instrumenSchoolSelect');
      if (instrSel) {
        const prev = instrSel.value;
        instrSel.innerHTML = optionsHtml;
        if (prev && Array.from(instrSel.options).some(o => o.value === prev)) {
          instrSel.value = prev;
        }
      }
    }

    function populateIndicatorSelect() {
      const pillar = document.getElementById('logPillar').value;
      const jenjang = appState.profile.jenjang || 'madya';
      const items = TUPOKSI_DATA[jenjang].pillars[pillar].items;
      const sel = document.getElementById('logIndicator');
      sel.innerHTML = items.map(it => `<option value="${escapeHtml(it)}">${escapeHtml(it)}</option>`).join('');
    }

    function renderLogs() {
      const search = (document.getElementById('searchLog').value || '').toLowerCase();
      const filterPillar = document.getElementById('filterLogPillar').value;

      document.getElementById('statTotal').textContent = appState.logs.length;
      document.getElementById('statPemantauan').textContent = appState.logs.filter(l => l.pillar === 'pemantauan').length;
      document.getElementById('statPenilaian').textContent = appState.logs.filter(l => l.pillar === 'penilaian').length;
      document.getElementById('statPembinaan').textContent = appState.logs.filter(l => l.pillar === 'pembinaan').length;

      const filtered = appState.logs.filter(l => {
        const matchPillar = filterPillar === 'all' || l.pillar === filterPillar;
        const matchSearch = !search ||
          l.schoolName.toLowerCase().includes(search) ||
          l.finding.toLowerCase().includes(search) ||
          l.rtl.toLowerCase().includes(search) ||
          l.indicator.toLowerCase().includes(search) ||
          (l.tahunPelajaran || '').toLowerCase().includes(search) ||
          (l.evidence || '').toLowerCase().includes(search);
        return matchPillar && matchSearch;
      });

      const container = document.getElementById('logListContainer');
      if (filtered.length === 0) {
        container.innerHTML = `
          <div class="text-center py-10 px-4 rounded-xl border border-dashed border-slate-300 text-slate-400 text-sm">
            Belum ada catatan pengawasan yang sesuai filter. Silakan tambahkan melalui formulir di samping.
          </div>
        `;
        return;
      }

      const pillarBadge = {
        pemantauan: '<span class="px-2.5 py-0.5 rounded-full text-[11px] font-bold bg-blue-100 text-blue-700">Pemantauan</span>',
        penilaian: '<span class="px-2.5 py-0.5 rounded-full text-[11px] font-bold bg-amber-100 text-amber-700">Penilaian</span>',
        pembinaan: '<span class="px-2.5 py-0.5 rounded-full text-[11px] font-bold bg-emerald-100 text-emerald-700">Pembinaan</span>'
      };

      container.innerHTML = filtered.map(log => {
        const scVal = Number(log.score) || 3;
        const sc = SCORE_RUBRIC[scVal] || SCORE_RUBRIC[3];
        const tpBadge = log.tahunPelajaran
          ? `<span class="px-2 py-0.5 rounded-md text-[11px] font-semibold bg-indigo-50 text-indigo-700 border border-indigo-100">TP ${escapeHtml(log.tahunPelajaran)}</span>`
          : '';
        const rawEv = (log.evidence || '').trim();
        const isUrl = /^https?:\/\//i.test(rawEv);
        const evidenceHtml = rawEv
          ? (isUrl
              ? `<a href="${escapeHtml(rawEv)}" target="_blank" rel="noopener noreferrer" class="text-indigo-600 hover:underline break-all font-medium">${escapeHtml(rawEv)}</a>`
              : `<span class="text-slate-700">${escapeHtml(rawEv)}</span>`)
          : `<span class="text-slate-400 italic">Belum ada bukti dukung dilampirkan</span>`;

        return `
          <article class="print-card rounded-xl border border-slate-200 p-4 bg-slate-50/50 hover:bg-white transition space-y-2.5">
            <div class="flex flex-wrap items-center justify-between gap-2">
              <div class="flex items-center gap-2 flex-wrap">
                ${pillarBadge[log.pillar]}
                ${tpBadge}
                <span class="text-xs font-bold text-slate-900">${escapeHtml(log.schoolName)}</span>
                <span class="text-xs text-slate-400">• ${log.date}</span>
              </div>
              <div class="flex items-center gap-2">
                <span class="px-2 py-0.5 rounded-md text-[11px] font-semibold bg-slate-200 text-slate-700">${escapeHtml(log.status)}</span>
                <button type="button" onclick="deleteLog('${log.id}')" class="no-print p-1 rounded-lg text-slate-400 hover:text-rose-600 hover:bg-rose-50 transition" title="Hapus catatan">
                  <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16" />
                  </svg>
                </button>
              </div>
            </div>

            <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-2 bg-indigo-50/70 px-3 py-2 rounded-lg">
              <p class="text-xs font-medium text-indigo-800">${escapeHtml(log.indicator)}</p>
              <span class="shrink-0 inline-flex items-center gap-1.5 px-2.5 py-1 rounded-lg text-[11px] font-bold border ${sc.badge}">
                Skor ${scVal}: ${sc.label}
              </span>
            </div>
            <p class="text-[11px] text-slate-500 px-1"><strong>Keterangan Skor:</strong> ${sc.desc}</p>

            <div class="grid grid-cols-1 sm:grid-cols-2 gap-2.5 text-xs">
              <div class="bg-white p-2.5 rounded-lg border border-slate-100">
                <span class="block font-semibold text-slate-500 mb-0.5">Temuan / Hasil:</span>
                <p class="text-slate-700 leading-relaxed">${escapeHtml(log.finding)}</p>
              </div>
              <div class="bg-white p-2.5 rounded-lg border border-slate-100">
                <span class="block font-semibold text-slate-500 mb-0.5">Rekomendasi / RTL:</span>
                <p class="text-slate-700 leading-relaxed">${escapeHtml(log.rtl)}</p>
              </div>
            </div>

            <div class="bg-white px-3 py-2 rounded-lg border border-slate-100 text-xs flex items-start gap-2">
              <svg class="w-4 h-4 text-indigo-500 shrink-0 mt-0.5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M15.172 7l-6.586 6.586a2 2 0 102.828 2.828l6.414-6.586a4 4 0 00-5.656-5.656l-6.415 6.585a6 6 0 108.486 8.486L20.5 13" />
              </svg>
              <div class="min-w-0">
                <span class="font-semibold text-slate-500">Bukti Dukung: </span>
                ${evidenceHtml}
              </div>
            </div>
          </article>
        `;
      }).join('');
    }

    function deleteLog(id) {
      appState.logs = appState.logs.filter(l => l.id !== id);
      renderLogs();
      showToast('Catatan pengawasan dihapus.');
    }

    function exportLogsCSV() {
      if (appState.logs.length === 0) {
        showToast('Belum ada data jurnal untuk diekspor.');
        return;
      }
      const headers = ['Tanggal', 'Tahun Pelajaran', 'Sekolah Binaan', 'Pilar', 'Butir Cakupan', 'Skor', 'Keterangan Skor', 'Temuan', 'Rekomendasi/RTL', 'Bukti Dukung', 'Status'];
      const rows = appState.logs.map(l => {
        const scVal = Number(l.score) || 3;
        const sc = SCORE_RUBRIC[scVal] || SCORE_RUBRIC[3];
        return [
          l.date,
          l.tahunPelajaran || appState.tahunPelajaran || '-',
          l.schoolName,
          l.pillar,
          l.indicator,
          scVal,
          `${sc.label} - ${sc.desc}`,
          l.finding,
          l.rtl,
          l.evidence || '-',
          l.status
        ].map(v => `"${String(v).replace(/"/g, '""')}"`).join(',');
      });

      const csv = [headers.join(','), ...rows].join('\n');
      const blob = new Blob([csv], { type: 'text/csv;charset=utf-8;' });
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url;
      a.download = `Jurnal_Pengawasan_${new Date().toISOString().split('T')[0]}.csv`;
      a.click();
      URL.revokeObjectURL(url);
      showToast('File CSV jurnal berhasil diunduh.');
    }

    // ==================== TAB 3: SEKOLAH BINAAN ====================
    function renderSchools() {
      document.getElementById('schoolCountBadge').textContent = `${appState.schools.length} Sekolah`;
      const container = document.getElementById('schoolListContainer');

      if (appState.schools.length === 0) {
        container.innerHTML = `<div class="col-span-full text-center py-8 text-sm text-slate-400 border border-dashed border-slate-300 rounded-xl">Belum ada sekolah binaan.</div>`;
      } else {
        container.innerHTML = appState.schools.map(s => `
          <div class="rounded-xl border border-slate-200 p-4 bg-slate-50/60 hover:bg-white transition flex flex-col justify-between gap-3">
            <div>
              <div class="flex items-start justify-between gap-2">
                <span class="px-2 py-0.5 rounded-md text-[11px] font-bold bg-indigo-100 text-indigo-700">${escapeHtml(s.level)}</span>
                <button type="button" onclick="deleteSchool('${s.id}')" class="text-slate-400 hover:text-rose-600 p-1 rounded-lg" title="Hapus sekolah">
                  <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                  </svg>
                </button>
              </div>
              <h4 class="font-bold text-slate-900 text-sm mt-2">${escapeHtml(s.name)}</h4>
              <p class="text-xs text-slate-500 mt-0.5">NPSN: ${escapeHtml(s.npsn || '-')} • KS: ${escapeHtml(s.principal)}</p>
            </div>
            <div class="text-[11px] font-medium text-emerald-700 bg-emerald-50 border border-emerald-100 px-2.5 py-1.5 rounded-lg">
              Prioritas: ${escapeHtml(s.priority)}
            </div>
          </div>
        `).join('');
      }
      populateSchoolSelect();
      renderTupoksiList();
    }

    function deleteSchool(id) {
      appState.schools = appState.schools.filter(s => s.id !== id);
      renderSchools();
      showToast('Sekolah binaan dihapus.');
    }

    // ==================== TAB 4: KALKULATOR ANGKA KREDIT ====================
    function renderAkCalculator() {
      const jenjang = document.getElementById('akJenjang').value;
      const cfg = TUPOKSI_DATA[jenjang];
      const initialAk = parseFloat(document.getElementById('akInitial').value) || 0;
      const hasBonus = document.getElementById('akEducationBonus').checked;
      const bonusAk = hasBonus ? (0.25 * cfg.minKP) : 0;

      let periodTotal = 0;
      const tbody = document.getElementById('akTableBody');

      if (appState.akPeriods.length === 0) {
        tbody.innerHTML = `<tr><td colspan="5" class="px-3 py-6 text-center text-slate-400">Belum ada periode penilaian ditambahkan.</td></tr>`;
      } else {
        tbody.innerHTML = appState.akPeriods.map(item => {
          const earned = (item.months / 12) * item.predikatVal * cfg.koefisien;
          periodTotal += earned;
          return `
            <tr class="hover:bg-slate-50">
              <td class="px-3 py-2.5 font-semibold text-slate-800">${escapeHtml(item.label)}</td>
              <td class="px-3 py-2.5 text-slate-600">${item.months} bln</td>
              <td class="px-3 py-2.5 text-slate-600">${escapeHtml(item.predikatLabel)}</td>
              <td class="px-3 py-2.5 text-right font-bold text-indigo-700">${formatNum(earned)}</td>
              <td class="px-3 py-2.5 text-center">
                <button type="button" onclick="deleteAkPeriod('${item.id}')" class="text-rose-500 hover:text-rose-700 font-semibold">Hapus</button>
              </td>
            </tr>
          `;
        }).join('');
      }

      const grandTotal = initialAk + periodTotal + bonusAk;

      document.getElementById('akTotalDisplay').textContent = formatNum(grandTotal);
      document.getElementById('akKoefDisplay').textContent = formatNum(cfg.koefisien);
      document.getElementById('akBonusDisplay').textContent = `+${formatNum(bonusAk)}`;

      const kpPct = Math.min(100, (grandTotal / cfg.minKP) * 100);
      document.getElementById('akKpText').textContent = `${formatNum(grandTotal)} / ${cfg.minKP}`;
      document.getElementById('akKpBar').style.width = `${kpPct}%`;
      const kpDiff = cfg.minKP - grandTotal;
      document.getElementById('akKpNote').textContent = kpDiff <= 0
        ? `Memenuhi syarat AK Kenaikan Pangkat (kelebihan ${formatNum(Math.abs(kpDiff))} AK).`
        : `Kurang ${formatNum(kpDiff)} AK lagi untuk kenaikan pangkat setingkat lebih tinggi.`;

      const kjBox = document.getElementById('akJenjangProgressBox');
      if (cfg.minKJ) {
        kjBox.classList.remove('hidden');
        const kjPct = Math.min(100, (grandTotal / cfg.minKJ) * 100);
        document.getElementById('akKjText').textContent = `${formatNum(grandTotal)} / ${cfg.minKJ}`;
        document.getElementById('akKjBar').style.width = `${kjPct}%`;
        const kjDiff = cfg.minKJ - grandTotal;
        const extraReq = jenjang === 'madya'
          ? ' Syarat tambahan ke Ahli Utama: Pendidikan minimal S-2 & lulus Uji Kompetensi.'
          : ' Wajib lulus Uji Kompetensi & tersedia formasi jabatan.';
        document.getElementById('akKjNote').textContent = kjDiff <= 0
          ? `Memenuhi syarat AK Kenaikan Jenjang!${extraReq}`
          : `Kurang ${formatNum(kjDiff)} AK lagi untuk kenaikan jenjang.${extraReq}`;
      } else {
        kjBox.classList.add('hidden');
      }
    }

    function deleteAkPeriod(id) {
      appState.akPeriods = appState.akPeriods.filter(p => p.id !== id);
      renderAkCalculator();
    }

    function clearAkPeriods() {
      appState.akPeriods = [];
      renderAkCalculator();
      showToast('Riwayat perhitungan AK direset.');
    }

    // ==================== UTILITIES ====================
    function formatNum(n) {
      return Number(n).toLocaleString('id-ID', { minimumFractionDigits: 2, maximumFractionDigits: 2 });
    }

    function escapeHtml(str) {
      return String(str)
        .replace(/&/g, '&amp;')
        .replace(/</g, '&lt;')
        .replace(/>/g, '&gt;')
        .replace(/"/g, '&quot;');
    }

    // ==================== EVENT LISTENERS & INIT ====================
    document.addEventListener('DOMContentLoaded', () => {
      // Login & Admin Tersembunyi (Klik Logo 3x)
      document.getElementById('formLogin').addEventListener('submit', handleLogin);
      document.getElementById('btnLogout').addEventListener('click', handleLogout);
      setupTripleClick('loginLogoTrigger', openAdminModal);
      setupTripleClick('headerLogoTrigger', openAdminModal);
      document.getElementById('btnCloseAdmin').addEventListener('click', closeAdminModal);

      document.getElementById('formAdminAddUser').addEventListener('submit', (e) => {
        e.preventDefault();
        const nip = document.getElementById('admNip').value.trim();
        const name = document.getElementById('admName').value.trim();
        const jenjang = document.getElementById('admJenjang').value;
        const gol = document.getElementById('admGol').value;
        const instansi = document.getElementById('admInstansi').value.trim();
        const errEl = document.getElementById('adminFormError');

        if (appState.registeredUsers.some(u => u.nip === nip)) {
          errEl.textContent = 'NIP tersebut sudah terdaftar dalam sistem.';
          errEl.classList.remove('hidden');
          return;
        }
        errEl.classList.add('hidden');

        appState.registeredUsers.push({ nip, name, jenjang, gol, instansi });
        renderAdminUsers();
        e.target.reset();
        document.getElementById('admInstansi').value = 'Dinas Pendidikan';
        showToast(`NIP ${nip} berhasil didaftarkan.`);
      });

      checkAuthState();

      // Default tanggal hari ini
      document.getElementById('logDate').value = new Date().toISOString().split('T')[0];

      // Navigasi Tab
      document.querySelectorAll('.nav-tab').forEach(btn => {
        btn.addEventListener('click', () => switchTab(btn.dataset.tab));
      });

      // Dropdown Sekolah pada Instrumen 16 Indikator
      document.getElementById('instrumenSchoolSelect').addEventListener('change', renderTupoksiList);

      // Modal Profil
      const modal = document.getElementById('profileModal');
      const openModal = () => {
        document.getElementById('profName').value = appState.profile.name;
        document.getElementById('profNip').value = appState.profile.nip;
        document.getElementById('profJenjang').value = appState.profile.jenjang;
        document.getElementById('profGol').value = appState.profile.gol;
        document.getElementById('profInstansi').value = appState.profile.instansi;
        modal.classList.remove('hidden');
        modal.classList.add('flex');
      };
      const closeModal = () => {
        modal.classList.add('hidden');
        modal.classList.remove('flex');
      };
      document.getElementById('btnOpenProfile').addEventListener('click', openModal);
      document.getElementById('btnCloseProfile').addEventListener('click', closeModal);
      document.getElementById('btnCancelProfile').addEventListener('click', closeModal);

      document.getElementById('formProfile').addEventListener('submit', (e) => {
        e.preventDefault();
        const oldNip = appState.profile.nip;
        appState.profile = {
          name: document.getElementById('profName').value.trim(),
          nip: document.getElementById('profNip').value.trim(),
          jenjang: document.getElementById('profJenjang').value,
          gol: document.getElementById('profGol').value,
          instansi: document.getElementById('profInstansi').value.trim()
        };
        const idx = appState.registeredUsers.findIndex(u => u.nip === oldNip);
        if (idx !== -1) {
          appState.registeredUsers[idx] = { ...appState.profile };
          currentSessionNip = appState.profile.nip;
        }
        renderProfile();
        document.getElementById('akJenjang').value = appState.profile.jenjang;
        selectAnalysisJenjang(appState.profile.jenjang);
        renderAkCalculator();
        closeModal();
        showToast('Profil pengawas diperbarui.');
      });

      // Modal Tahun Pelajaran Manual
      const tpModal = document.getElementById('tpModal');
      const openTpModal = () => {
        document.getElementById('inputTahunPelajaran').value = appState.tahunPelajaran || '2026/2027';
        tpModal.classList.remove('hidden');
        tpModal.classList.add('flex');
      };
      const closeTpModal = () => {
        tpModal.classList.add('hidden');
        tpModal.classList.remove('flex');
      };
      document.getElementById('btnOpenTp').addEventListener('click', openTpModal);
      document.getElementById('btnCloseTp').addEventListener('click', closeTpModal);
      document.getElementById('btnCancelTp').addEventListener('click', closeTpModal);

      document.getElementById('formTp').addEventListener('submit', (e) => {
        e.preventDefault();
        const newTp = document.getElementById('inputTahunPelajaran').value.trim();
        if (!newTp) return;
        appState.tahunPelajaran = newTp;
        renderTahunPelajaran();
        closeTpModal();
        showToast(`Tahun Pelajaran diatur ke ${newTp}`);
      });

      // Form Jurnal Pengawasan
      document.getElementById('logPillar').addEventListener('change', populateIndicatorSelect);
      document.getElementById('formLog').addEventListener('submit', (e) => {
        e.preventDefault();
        const checkedScore = document.querySelector('input[name="logScore"]:checked');
        const scoreVal = checkedScore ? parseInt(checkedScore.value, 10) : 3;
        const newLog = {
          id: 'log-' + Date.now(),
          date: document.getElementById('logDate').value,
          tahunPelajaran: appState.tahunPelajaran || '2026/2027',
          schoolName: document.getElementById('logSchool').value,
          pillar: document.getElementById('logPillar').value,
          indicator: document.getElementById('logIndicator').value,
          score: scoreVal,
          finding: document.getElementById('logFinding').value.trim(),
          rtl: document.getElementById('logRtl').value.trim(),
          evidence: document.getElementById('logEvidence').value.trim(),
          status: document.getElementById('logStatus').value
        };
        appState.logs.unshift(newLog);
        renderLogs();
        document.getElementById('logFinding').value = '';
        document.getElementById('logRtl').value = '';
        document.getElementById('logEvidence').value = '';
        showToast('Kegiatan pengawasan berhasil dicatat.');
      });

      document.getElementById('searchLog').addEventListener('input', renderLogs);
      document.getElementById('filterLogPillar').addEventListener('change', renderLogs);

      // Form Sekolah Binaan
      document.getElementById('formSchool').addEventListener('submit', (e) => {
        e.preventDefault();
        const newSchool = {
          id: 'sch-' + Date.now(),
          name: document.getElementById('schoolName').value.trim(),
          level: document.getElementById('schoolLevel').value,
          npsn: document.getElementById('schoolNpsn').value.trim(),
          principal: document.getElementById('schoolPrincipal').value.trim(),
          priority: document.getElementById('schoolPriority').value
        };
        appState.schools.push(newSchool);
        renderSchools();
        e.target.reset();
        showToast('Sekolah binaan berhasil ditambahkan.');
      });

      // Form Kalkulator AK
      document.getElementById('akJenjang').value = appState.profile.jenjang;
      ['akJenjang', 'akInitial', 'akEducationBonus'].forEach(id => {
        document.getElementById(id).addEventListener('input', renderAkCalculator);
        document.getElementById(id).addEventListener('change', renderAkCalculator);
      });

      document.getElementById('formAkPeriod').addEventListener('submit', (e) => {
        e.preventDefault();
        const sel = document.getElementById('akPredikat');
        appState.akPeriods.push({
          id: 'ak-' + Date.now(),
          label: document.getElementById('akYearLabel').value.trim(),
          months: parseInt(document.getElementById('akMonths').value, 10) || 12,
          predikatVal: parseFloat(sel.value),
          predikatLabel: sel.options[sel.selectedIndex].text
        });
        renderAkCalculator();
        showToast('Periode konversi AK ditambahkan.');
      });

      // Render awal
      renderProfile();
      renderSchools();
      renderTahunPelajaran();
      selectAnalysisJenjang(appState.profile.jenjang || 'madya');
      renderLogs();
      renderAkCalculator();
    });
  </script>
</body>
</html>
