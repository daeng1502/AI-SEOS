# Human Interaction Playbook (Human-in-the-Loop)

Version: 1.0
Status: Final

---

# Purpose

Playbook ini mendefinisikan langkah-langkah kerja taktis bagi AI Agent ketika menghadapi ambiguitas, konflik, atau kendala teknis penting yang memerlukan klarifikasi dan keputusan dari manusia (Project Owner/Stakeholder).

---

# Objective

- Menyediakan alur terstruktur untuk mendeteksi kendala/blocker.
- Menstandarkan pengajuan pertanyaan klarifikasi dari AI Agent ke manusia.
- Memastikan keputusan yang diambil manusia tercatat kembali ke dalam *Source of Truth* (`project-knowledge.md`).
- Menjamin kelancaran kelanjutan eksekusi setelah keputusan diperoleh.

---

# Inputs

- Blocker / Ambiguity / Conflict (dari kode, standard, atau kebutuhan)
- Project Knowledge (`project-knowledge.md`)
- srs.md

---

# Outputs

- Clarification Request (menggunakan templat)
- Updated `project-knowledge.md`
- Resolved Blocker

---

# Execution Steps

1. **Identifikasi Blocker**: Deteksi apakah terdapat ketidakpastian, konflik kebutuhan, atau hambatan teknis yang memenuhi Kriteria Halt pada `human-in-the-loop.md` (Standard).
2. **Kategorisasi Urgensi**: Tentukan tingkat keparahan kendala (Low, Medium, atau High).
3. **Susun Dokumen Klarifikasi**: Buat draf pengajuan pertanyaan menggunakan berkas **[clarification-request-template.md](file:///E:/Project/AI-SEOS/AI-SEOS/templates/clarification-request-template.md)**. Pastikan mencantumkan minimal 2 opsi solusi beserta keuntungan/kerugian masing-masing.
4. **Kirim Pertanyaan & Kelola Status**:
   - Jika **HIGH (Blocker)**: Hentikan seluruh proses eksekusi rekayasa dan tunggu hingga manusia memberikan respon.
   - Jika **LOW/MEDIUM**: Kirim pertanyaan, lanjutkan pengerjaan tugas (*Tasks*) lain yang paralel jika memungkinkan.
5. **Terima Keputusan**: Baca jawaban/keputusan dari manusia secara saksama.
6. **Perbarui Source of Truth**:
   - Tulis keputusan baru tersebut ke dalam dokumen **`project-knowledge.md`** di bagian *Business Rules* atau *Technical Knowledge*.
   - Tingkatkan versi berkas *Knowledge* (misalnya dari v1.4 ke v1.5) untuk menjaga *versioning*.
7. **Perbarui Dokumen Turunan**: Selaraskan berkas `srs.md` atau `project-plan.md` yang terdampak oleh keputusan tersebut.
8. **Lanjutkan Eksekusi**: Lanjutkan tugas yang sempat tertunda dengan mengacu pada aturan baru yang telah disetujui.

---

# Completion Criteria

- Masalah klarifikasi telah dijawab oleh manusia.
- Keputusan manusia telah terintegrasi di `project-knowledge.md`.
- Tugas rekayasa perangkat lunak dilanjutkan berdasarkan aturan baru.

---

# Deliverables

- Clarification Request Document
- Updated Project Knowledge File

---

# References

- human-in-the-loop.md (Standard)
- clarification-request-template.md (Template)
- KNOWLEDGE.md

---

# Version History

| Version | Description |
|----------|-------------|
| 1.0 | Initial Human Interaction Playbook |
