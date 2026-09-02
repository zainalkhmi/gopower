# GOパワーシミュレーターⅡ｜詳細診断版 (GoPower Simulator II - Pro)

Aplikasi simulasi dan kalkulator investasi pembangkit listrik tenaga surya (PV) dan sistem baterai penyimpanan energi (BESS) untuk bangunan komersial & industri (Pabrik, Gudang, Kantor, Rumah Sakit, dll.) dengan fitur diagnosis menyeluruh dan penilaian insentif pajak perusahaan Jepang.

## 🚀 Fitur Utama
1. **Identifikasi Objek Properti & Pengukuran Luas Atap**:
   - Pencarian alamat properti dengan integrasi Google Maps JavaScript SDK (Geocoder + Geometry).
   - Pengukuran poligon atap secara langsung via citra satelit (`🗺️ 航空写真で実測`) atau input manual.
   - Koefisien efisiensi atap otomatis (Folded Plate 0.65, Gabled 0.45, Flat Roof 0.55, Flat Concrete 0.60).
2. **Kalkulasi Konsumsi & Penghematan Listrik**:
   - Perhitungan estimasi produksi listrik tahunan berdasarkan lokasi & jenis bangunan.
   - Perhitungan rasio konsumsi mandiri (*self-consumption rate*) dengan sistem baterai.
3. **Kalkulasi BCP (Business Continuity Plan) & Beban Kritis**:
   - Pemilihan peralatan kritis (Kulkas/Pendingin, Panel Kontrol, Telekomunikasi, Pencahayaan, Pompa, dll.).
   - Estimasi durasi proteksi saat pemadaman listrik & nilai penghindaran kerugian operasional.
4. **Penilaian Insentif Pajak Korporasi (法人税制優遇制度)**:
   - Evaluasi kelayakan *SME Management Enhancement Tax System* (中小企業経営強化税制 A類型).
   - Perbandingan strategi: Prioritas Likuiditas/Arus Kas (即時償却 - Amortisasi Cepat) vs Prioritas Total Potongan Pajak (税額控除 10% - Pengurangan Pajak Tetap).
   - Checklist persyaratan pengajuan pajak.
5. **Simulasi Keuangan 20 Tahun & Grafik Arus Kas**:
   - Visualisasi grafik *20-Year Cumulative Cash Flow* interaktif menggunakan Recharts.
   - Kalkulasi Payback Period standar dan Payback Period setelah insentif pajak.
6. **Ekspor Laporan & Proposal**:
   - Generate proposal presentasi PowerPoint (`.pptx`) otomatis via `pptxgenjs`.
   - Download laporan proposal PDF resmi via `jspdf` & `html2canvas`.

---

## 🛠️ Cara Menjalankan Secara Lokal

### Menggunakan Node.js / npx:
```bash
# Menggunakan npx serve
npx serve . -p 3000

# Atau menggunakan npm
npm run dev
```

Buka browser di `http://localhost:3000`.

---

## 📁 Struktur File
- [`index.html`](file:///c:/Users/ndens/gopower/index.html): Kode lengkap aplikasi (React, Tailwind CSS, Recharts, Babel, jsPDF, html2canvas, pptxgenjs, Google Maps SDK, dan aset logo base64).
- [`package.json`](file:///c:/Users/ndens/gopower/package.json): Konfigurasi package dan script dev server lokal.
- [`vercel.json`](file:///c:/Users/ndens/gopower/vercel.json): Konfigurasi routing untuk deployment ke Vercel.
