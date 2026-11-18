# Wealthplanner Financial Calculator — Handoff

Isi ZIP:
- `mockup/index.html`: mockup halaman kalkulator, buka langsung di browser.
- `app/`: starter React + TypeScript dengan 9 calculator tiles dan simulasi dasar.
- `calculator-excel/wealthplanner-financial-calculators.xlsx`: workbook 9 worksheet.
- `copywriting/ui-copy.md`: wording UI dan disclaimer.
- `docs/FORMULA-AND-ASSUMPTIONS.md`: formula dan batasan model.

## Jalankan app
Butuh Node.js 18+. Di folder `app`: `npm install`, lalu `npm run dev`.
Paket ini belum mengubah GitHub/Vercel dan bukan deployment otomatis.

## Acuan app saat ini
Repo: `jasminework2023/personal-wealthplanner`
File: `src/pages/FinancialCalculator.tsx`
https://github.com/jasminework2023/personal-wealthplanner/blob/main/src/pages/FinancialCalculator.tsx

Calculator di app acuan: Financial Check-Up, KPR, Dana Pendidikan, Dana Pensiun, Warisan, Haji & Umrah, Zakat & Wakaf, Investasi, Kebutuhan Asuransi.

Catatan: starter code dan workbook ini adalah handoff awal, bukan salinan tersertifikasi dari seluruh logika production. Developer perlu membandingkan formula per calculator dengan source app dan menjalankan regression test sebelum merge/deploy.

## UI refresh — conversational flow
- Form pada kalkulator di `app/src/App.tsx` sekarang memakai pola satu pertanyaan per langkah.
- Setelah nilai valid diketik dan pengguna berhenti mengetik sebentar, pertanyaan berikutnya terbuka otomatis; tombol Lanjutkan tetap tersedia sebagai alternatif.
- Jawaban sebelumnya tetap terlihat dan dapat dipilih untuk diedit.
- Anggaran Keuangan mempertahankan alur serta laporan existing, dengan auto-advance pada isian yang valid.
- Styling baru mengikuti referensi konsultasi-asuransi: warm cream, off-white, green, brown accent, rounded cards, dan responsive layout.
- Fungsi kalkulasi di `app/src/calc.ts` tidak diubah.

Jalankan dari folder `app` dengan `npm install` lalu `npm run dev`. Jalankan `npm run build` dan regression test kalkulator sebelum merge/deploy.
