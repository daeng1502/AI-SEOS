# Project Discovery Standard

Version: 1.0
Status: Final

---

# Purpose

Standar ini mendefinisikan aturan kelayakan dan tingkat kelengkapan informasi yang wajib diperoleh selama fase inisiasi proyek (*Project Discovery*). Standar ini memastikan AI Agent memiliki data bisnis awal yang valid sebelum memulai analisis kebutuhan teknis (*Requirement Analysis*).

---

# Objective

- Menstandarkan kriteria kelayakan masukan informasi awal proyek.
- Menjamin tidak ada data bisnis krusial yang terlewat pada awal kolaborasi.
- Menetapkan *Definition of Ready* (DoR) yang jelas sebelum memulai tahap SRS.
- Mencegah inkonsistensi asumsi antara AI Agent dan manusia mengenai batasan proyek.

---

# General Principles

- Data Sufficiency (Kecukupan Data Minimum)
- Source Validation (Validitas Sumber Informasi)
- Strategic Alignment (Keselarasan Masalah dan Solusi)
- Consensus (Kesepakatan Batas Scope Proyek)

---

# Kebutuhan Informasi Minimum (*Minimum Information Requirements*)

Sebuah sesi *Project Discovery* dinyatakan memenuhi standar kualitas hanya jika berhasil mengumpulkan informasi berikut secara lengkap:

1. **Profil Proyek**: Nama resmi proyek, singkatan, domain bisnis, dan pemilik/pengelola proyek.
2. **Peta Stakeholder**: Daftar peran pengguna sistem saat ini (*As-Is*) dan peran yang akan diimplementasikan di dalam sistem (*To-Be*) beserta wewenangnya.
3. **Identifikasi Masalah (*Pain Points*)**: Minimal 3 pernyataan masalah operasional/bisnis konkret yang sedang terjadi pada proses berjalan.
4. **Sasaran Bisnis (*Objectives*)**: Pernyataan tujuan strategis yang terukur tentang bagaimana sistem akan memecahkan masalah tersebut.
5. **Batasan Proyek (*Scope Boundaries*)**: Daftar modul/fitur yang masuk dalam batas pengerjaan (*In-Scope*) dan yang tidak dikerjakan (*Out-of-Scope*).
6. **Lingkungan Teknis (*Constraints*)**: Pilihan teknologi utama (bahasa pemrograman, framework, database), infrastruktur hosting, integrasi, dan batasan bahasa.

---

# Aturan Validasi Informasi

AI Agent wajib melakukan validasi silang (*cross-validation*) untuk mendeteksi kontradiksi informasi bisnis:
- **Validasi Masalah vs Fitur**: Setiap fitur utama yang diusulkan masuk *In-Scope* harus dapat ditelusuri ke minimal satu masalah operasional yang diidentifikasi.
- **Validasi Peran**: Setiap peran pengguna dalam sistem (*To-Be*) harus memiliki wewenang atau tanggung jawab aksi yang jelas.

---

# Definition of Ready (DoR) untuk Requirement Analysis

Fase *Project Discovery* dinyatakan selesai dan proyek siap beralih ke tahap *Requirement Analysis* jika dan hanya jika:
- Dokumen **`project-knowledge.md`** telah terisi penuh sesuai standar informasi minimum.
- Dokumen **`project-plan.md`** telah diisi, diverifikasi, dan mendapat **persetujuan formal** (status *Approved*) dari *Project Owner*.

---

# Deliverables

- Completed Project Knowledge File
- Approved Initial Project Plan

---

# References

- KNOWLEDGE.md
- PROJECTS.md
- project-plan-template.md
- project-initiation.md (Playbook)

---

# Version History

| Version | Description |
|----------|-------------|
| 1.0 | Initial Project Discovery Standard |
