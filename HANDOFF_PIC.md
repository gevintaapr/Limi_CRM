# Serah Terima UI Limitless Hub, per PIC

**Lokasi:** `D:\Documents\DPP\ui\` (buka `index.html`) · arah visual **Botanical Ledger** · frame desktop **1440 × 1024**.
**Acuan isi:** `Spesifikasi_Fungsional_Limitless_Hub_v2.md` (kode modul M-xx dan FR-xx).

## Cara memindahkan ke Figma (file "CRM")
1. Di file Figma, buat halaman: `00 Design System`, `Gevi`, `Gita`, `Agna`, `Han`, `Prototype`.
2. Buka layar HTML di Chrome. Untuk file lokal, aktifkan "Allow access to file URLs" pada ekstensi.
3. Impor dengan plugin/ekstensi **html.to.design** ke halaman milik PIC. Gunakan lebar 1440, kecuali `19-pelanggan-qr` yang lebarnya 1760.
4. Setelah diimpor, rapikan auto-layout, lalu ganti elemen berulang (tombol, tag, input, ledger KPI, item sidebar) dengan **komponen** dari `00 Design System`.
5. Ikon memakai set **Lucide** (stroke 1.75). Font: **Fraunces** (judul/angka) dan **Inter** (UI).

## Aturan bersama
- Warna hanya dari token: Forest, Moss, Sage, Oak, Ivory, Stone, Surface, Ink, dan warna semantik (lihat `01-design-system`). Oak dipakai hemat, sekitar 10%.
- Status selalu memakai **ikon + teks**, tidak hanya warna. Kontras teks ≥ 4,5:1.
- Maskot hanya untuk momen: login, onboarding, tips, pengingat, sukses, empty state. **Maksimal 1 per layar**, tidak di tabel atau grafik padat.
  Pose: `wave` sapaan · `happy` sukses · `wink` tips · `wow` pencapaian/empty · `cheer` pengingat · `upset` perhatian/error.
- Data di layar adalah data contoh. Angka yang berasal dari wawancara (diskon 15%, kompensasi 20%/32%, Google Maps paling efektif) jangan diubah.

## Gevi: Design System, Login, Dashboard & Kalender (M-09), Pengaturan (M-10)
Layar: 01, 02, 03, 04, 05
- Ubah `01` menjadi library komponen beserta variannya (state default/hover/disabled/focus).
- Login: tambah state salah kata sandi (maskot `upset`) dan lupa kata sandi.
- Dashboard: tambah versi **Kepala Unit** (fokus keluhan unit + kalender) dan versi **Marketing** (kampanye + kanal).
- Kalender: tambah tampilan minggu dan modal "Tambah agenda".
- Pengaturan: tab Staf & peran, Unit & outlet (siap Bali/Gombor), Privasi & data, Log.

## Gita: Customer 360 & Lookup (M-03), Program Kampus (M-04), Integrasi POS (M-02)
Layar: 06, 07, 08, 09, 10
- Lookup: tambah state "tidak ditemukan" (maskot `wink`, ajak daftar via QR struk) dan toast sukses verifikasi (maskot `happy`).
- Profil 360: tab Transaksi, Voucher, Masukan, Catatan, Privasi (alur hapus data dengan dialog konfirmasi).
- Customer 360: panel filter lanjutan (kampus, sumber, tag, rentang belanja).
- Integrasi POS: alur unggah CSV (pilih file → pratinjau → pemetaan → hasil) dan state error koneksi (maskot `upset`).

## Agna: Kampanye WA & ROI (M-05), Reward & Voucher (M-06)
Layar: 11, 12, 13, 14
- Wizard kampanye: buat langkah 1 (Tujuan), 3 (Penawaran & pesan + pratinjau bubble WhatsApp), dan 4 (Tinjau & jadwal).
- Laporan: tambahkan perbandingan antarkampanye.
- Voucher: modal "Terbitkan voucher" dan "Reward baru"; detail voucher (riwayat pakai dari POS).
- Empty state kampanye pertama (maskot `wow`).

## Han: Review & Keluhan (M-07), Event & Mitra (M-08), Halaman Pelanggan (M-01)
Layar: 15, 16, 17, 18, 19
- Keluhan: tab Diproses/Selesai beserta hasil pemulihan (voucher dipakai? kembali?), alur eskalasi, dan modal "Input review Google".
- Event: tampilan Kalender, form "Lead baru", dan detail mitra.
- Halaman pelanggan: state nomor struk tidak valid/sudah dipakai, OTP salah, cek status member/voucher, dan versi QR kartu meja (masukan saja).

## Prototype (bersama, untuk video)
Sambungkan alur di halaman `Prototype` sesuai skenario "satu sore saat sunset":
UF-1 daftar via QR (19) → UF-2 verifikasi KTM (06) → keluhan masuk (19 → 15) → UF-5 kampanye (11 → 12 → 13) → UF-6 event (16 → 17) → UF-7 dashboard (03 → 04).
