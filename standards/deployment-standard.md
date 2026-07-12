# Deployment Standard

Version: 1.0
Status: Final

---

# Purpose

Standar ini mendefinisikan prosedur dan aturan rilis (deployment) aplikasi guna meminimalkan downtime, mendokumentasikan perubahan versi, dan menjaga stabilitas lingkungan produksi (production environment).

---

# Objective

- Menjamin kelancaran proses rilis ke lingkungan server.
- Mencegah kehilangan data selama migrasi database.
- Menyediakan prosedur penanganan kegagalan rilis (rollback).
- Menstandarkan sistem penomoran rilis (versioning).

---

# General Principles

- Automated First
- Risk Mitigation (Mitigasi Risiko)
- Zero Downtime (diupayakan)
- Traceability of Release
- Environment Separation (Pemisahan Lingkungan)

---

# Environment Separation Rules

Pengembangan wajib dipisahkan minimal ke dalam tiga lingkungan terisolasi:
1. **Development (Dev)**: Lingkungan uji coba lokal bagi tim pengembang.
2. **Staging (Stg)**: Lingkungan yang identik dengan produksi untuk keperluan pengujian akhir (QA) dan validasi user (UAT).
3. **Production (Prod)**: Lingkungan rilis publik yang digunakan oleh pengguna akhir.

---

# Versioning Rules (Semantic Versioning 2.0.0)

Format versi wajib mengikuti aturan `MAJOR.MINOR.PATCH`:
- **MAJOR**: Perubahan besar yang tidak kompatibel dengan versi sebelumnya (breaking changes).
- **MINOR**: Penambahan fitur baru yang kompatibel dengan versi sebelumnya.
- **PATCH**: Perbaikan bug atau patch keamanan yang kompatibel dengan versi sebelumnya.

---

# Database Migration Rules

- **No Destructive Direct Commands**: Dilarang melakukan manipulasi skema database secara langsung pada database server produksi (seluruh perubahan wajib melalui skrip migrasi terkomputerisasi).
- **Backup Before Migration**: Backup basis data produksi secara penuh wajib dilakukan sebelum menjalankan skrip migrasi baru.
- **Rollback Script**: Setiap file migrasi database baru wajib memiliki skrip pembatalan (*down/rollback script*).

---

# Verification Rules (Smoke Testing)

Setelah proses deployment selesai pada server tujuan, tim pengembang wajib melakukan verifikasi dasar:
- Memastikan halaman login utama dapat diakses.
- Memeriksa konektivitas database (membaca satu tabel master).
- Memeriksa integrasi pihak ketiga (Payment Gateway, API LLM) berjalan tanpa error 500.

---

# Deliverables

- Deployment Plan Document
- Environment Configuration Template (.env.example)
- Release Notes

---

# References

- maintenance-standard.md
- deployment-plan-template.md

---

# Version History

| Version | Description |
|----------|-------------|
| 1.0 | Initial Deployment Standard |
