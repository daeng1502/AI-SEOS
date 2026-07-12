# Human-in-the-Loop (HITL) Standard

Version: 1.3
Status: Final

---

# Purpose

Standar ini mendefinisikan aturan, kriteria, dan etika kolaborasi antara AI Agent dan manusia (Project Owner/Stakeholder). Standar ini memastikan bahwa AI tidak membuat keputusan penting secara sepihak ketika menghadapi ketidakpastian dalam proses software engineering.

---

# Objective

- Mencegah kesalahan implementasi akibat asumsi sepihak oleh AI.
- Menjamin setiap keputusan krusial terdokumentasi dan disetujui manusia.
- Menstandarkan cara komunikasi AI kepada manusia agar efisien.
- Menetapkan jalur eskalasi (*escalation path*) yang jelas saat terjadi kendala.

---

# General Principles

- Human Sovereignty (Kedaulatan Manusia sebagai Pengambil Keputusan)
- Transparency (Transparansi Masalah dan Opsi)
- Traceability (Keterlacakan Keputusan)
- Context-Rich Communication (Komunikasi yang Kaya Konteks)

---

# Kriteria Halt (Kapan AI Wajib Berhenti)

AI Agent **wajib menghentikan pekerjaan** dan berdiskusi dengan manusia apabila menemui kondisi berikut:

1. **Ambiguitas Kebutuhan (Ambiguity)**: Ada persyaratan dari stakeholder yang dapat ditafsirkan secara ganda atau tidak memiliki detail yang cukup untuk diimplementasikan.
2. **Aturan Bisnis Kontradiktif (Conflict)**: Terdapat dua atau lebih *Business Rules* yang bertentangan satu sama lain.
3. **Pilihan Arsitektur/Teknis Kritis (Trade-offs)**: Pilihan antara teknologi atau pola desain yang memiliki kelebihan dan kekurangan yang berimbang (misal: memilih SQL vs NoSQL).
4. **Kegagalan Infrastruktur Kritis (Blockers)**: Terjadi masalah teknis di luar kendali AI (misal: API pihak ketiga tidak merespon, server tidak bisa diakses).
5. **Perubahan Scope Tengah Jalan (Change Request)**: Manusia meminta fitur baru yang secara signifikan memengaruhi rancangan arsitektur atau rencana proyek yang sudah disetujui.
6. **Ketiadaan Informasi Proses Bisnis (Strict Ignorance)**: Terjadi kekosongan atau ketidakjelasan informasi mengenai mekanisme proses bisnis manual (As-Is). AI dilarang menebak/mengasumsikan detailnya menggunakan pengetahuan umum bawaan, melainkan wajib berhenti untuk meminta penegasan atau membiarkannya tidak terdefinisi sesuai kenyataan lapangan.

---

# [RULE-HITL-001] Prinsip Asumsi Nihil (Strict Ignorance Constraint)

AI Agent terikat oleh kewajiban kepatuhan mutlak terhadap batasan informasi tertulis:
- **Dilarang Menambah Asumsi**: AI Agent dilarang keras menambahkan langkah aktivitas, aktor, media komunikasi (seperti jenis aplikasi chat), dokumen, atau mekanisme transaksi yang tidak terdokumentasi di dalam `project-knowledge.md`.
- **Halt atau Biarkan Kosong**: Jika menemukan celah informasi, AI Agent wajib menyatakannya secara jujur sebagai "tidak terdokumentasi/informal" atau melakukan *Halt* untuk bertanya, bukan berspekulasi menggunakan basis pengetahuan eksternal LLM.

---

# [RULE-HITL-002] Rekonsiliasi Batas Fase (Phase Gate Reconciliation)

AI Agent wajib melakukan prosedur penutupan fase kerja secara transparan dan terstruktur sebelum melangkah ke perencanaan fase baru untuk mencegah celah proses (process slip):
- **Penyajian Tabel Rekonsiliasi**: Sebelum mengajukan perpindahan fase/tahap kerja baru kepada pengguna, AI Agent wajib menyajikan Tabel Rekonsiliasi Cakupan di chat. Tabel ini harus mencocokkan jumlah entitas/persyaratan di dokumen dasar (seperti SRS) dengan hasil pengerjaan nyata di repositori lokal.
- **Persetujuan Handshake Eksplisit**: AI Agent dilarang keras merancang atau mengajukan Implementation Plan untuk fase baru sebelum mendapatkan konfirmasi persetujuan tertulis dari pengguna berupa pernyataan bahwa fase saat ini telah selesai sepenuhnya.

---

# [RULE-HITL-003] Isolasi Diskusi Multi-Item (Isolated Multi-Item Discussion)

AI Agent wajib melakukan diskusi secara berurutan dan terisolasi ketika membahas banyak item/tabel/fitur sekaligus untuk mencegah terlewatnya detail penting:
- **Satu Putaran Satu Item**: AI Agent dilarang mengajukan pertanyaan atau opsi perubahan untuk lebih dari satu entitas/tabel dalam satu putaran percakapan (one turn), kecuali jika pengguna secara eksplisit meminta pembahasan kolektif.
- **Pencegahan Bias Efisiensi**: AI Agent dilarang mempercepat diskusi dengan merangkum atau melompati daftar urutan demi efisiensi waktu, karena ketelitian pemeriksaan manusia jauh lebih diprioritaskan daripada kecepatan pengerjaan AI.

---

# Tingkat Urgensi Pertanyaan

Setiap pengajuan pertanyaan oleh AI wajib menyertakan tingkat urgensi:
- **LOW**: Pertanyaan klarifikasi kecil yang tidak menahan proses implementasi utama (dapat dijawab nanti).
- **MEDIUM**: Memengaruhi detail fitur tertentu, menahan satu tugas (*Task*), tetapi AI masih bisa mengerjakan tugas lain yang paralel.
- **HIGH (Blocker)**: Memengaruhi arsitektur inti atau kelangsungan seluruh proyek. AI harus berhenti total sampai ada jawaban.

---

# Aturan Pengajuan Pertanyaan

Setiap pertanyaan yang diajukan AI kepada manusia wajib mematuhi aturan berikut:
- Menggunakan format resmi **[clarification-request-template.md](file:///E:/Project/AI-SEOS/AI-SEOS/templates/clarification-request-template.md)**.
- Menyediakan minimal 2 opsi solusi yang konkret beserta dampak (*pros & cons*) masing-masing.
- Memberikan rekomendasi teknis terbaik dari sudut pandang AI beserta alasannya.
- Bahasa yang digunakan harus sopan, jelas, dan menggunakan Bahasa Indonesia yang mudah dipahami non-teknis (untuk aspek bisnis).

---

# Deliverables

- Clarification Request Record
- Decision Log Update

---

# References

- validation-rules.md
- clarification-request-template.md
- human-interaction.md (Playbook)

---

# Version History

| Version | Description |
|----------|-------------|
| 1.0 | Initial Human-in-the-Loop Standard |
| 1.1 | Penambahan [RULE-HITL-001] Prinsip Asumsi Nihil (Strict Ignorance Constraint) |
| 1.2 | Penambahan [RULE-HITL-002] Rekonsiliasi Batas Fase (Phase Gate Reconciliation) |
| 1.3 | Penambahan [RULE-HITL-003] Isolasi Diskusi Multi-Item (Isolated Multi-Item Discussion) |
