# AI-SEOS - Improvement Backlog (Catatan Pengembangan)

> **⚠️ PERINGATAN UNTUK AI AGENT (CRITICAL SYSTEM RULE):**
> Berkas ini HANYALAH catatan draf (draft) atau *backlog* ide untuk masa depan. **DILARANG KERAS** menjadikan isi berkas ini sebagai pedoman kerja (guideline), aturan (rules), atau referensi aktif saat Anda menulis kode atau mengeksekusi *workflow* AI-SEOS. Ide di sini tidak berlaku sampai pengguna secara eksplisit memindahkannya ke berkas konfigurasi resmi (seperti `AGENTS.md` atau `GOVERNANCE.md`).

---

## Tujuan Dokumen
Berkas ini digunakan sebagai wadah penampungan (keranjang) untuk mencatat ide-ide brilian, celah pengembangan, atau hipotesis yang muncul selama diskusi antara *Human* (Arsitek) dan *AI Agent*. 

Ketika *Human* siap untuk melakukan pembaruan (Upgrade) pada versi AI-SEOS, kita hanya perlu membuka kembali catatan ini untuk meninjau mana yang layak diimplementasikan.

---

## 📝 Daftar Ide & Celah Pengembangan (Draft)

### 1. [Contoh] Peningkatan Sistem "Proactive Knowledge Extraction"
- **Konteks**: Saat ini AI sudah diinstruksikan proaktif lewat `AGENTS.md`. 
- **Ide Pengembangan**: Di masa depan, mungkin AI-SEOS perlu memiliki format *template* khusus (misalnya `knowledge-proposal.yaml`) agar saat AI menawarkan penyimpanan *knowledge*, format laporannya seragam dan mudah dibaca oleh skrip CI/CD.
- **Status**: Menunggu peninjauan.

### 2. Peningkatan Manajemen State Sesi & Pemulihan Progress Otomatis (Session State Auto-Backup)
- **Konteks**: Kejadian pengguna secara tidak sengaja menutup sesi/IDE (*human error* atau pemadaman listrik) menimbulkan kekhawatiran hilangnya progres pengerjaan yang sedang berjalan.
- **Ide Pengembangan**: AI-SEOS sebaiknya menyediakan mekanisme pencatatan berkala (*session snapshotting*) ke berkas lokal tersembunyi (misal `.agents/session-checkpoint.json`) yang mencatat checkpoint terakhir, task.md yang aktif, dan file terakhir yang sedang diedit. Saat sesi baru dimulai, agen dapat langsung memulihkan status pengerjaan secara mandiri tanpa meminta penjelasan ulang dari pengguna.
- **Status**: Menunggu peninjauan.

### 3. Pemetaan Aturan Lokal Dinamis (Dynamic Custom Rules Mapping)
- **Konteks**: Saat ini agen diinstruksikan secara global untuk membaca aturan sub-proyek secara manual.
- **Ide Pengembangan**: Mengembangkan modul loader pada AI-SEOS yang secara otomatis menginjeksi berkas aturan lokal (seperti `silatrasa-rules.md` atau `project-rules.md`) ke dalam instruksi utama (*system prompt*) secara dinamis hanya jika *current working directory* (Cwd) agen berada di bawah folder proyek yang bersangkutan, guna menghindari polusi konteks global.
- **Status**: Menunggu peninjauan.
