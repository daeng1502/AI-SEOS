# AI-SEOS - Global Agent Rules (Workspace Customization)

Berkas ini adalah konfigurasi aturan AI tingkat-akar (root) untuk repositori `AI-SEOS`. Karena repositori ini dapat memuat banyak sub-proyek di dalam folder `outputs/` maupun `examples/`, agen AI WAJIB mematuhi isolasi proyek berikut:

## 1. Isolasi Konteks (Mencegah Halusinasi Lintas Proyek)
- **Fokus Proyek**: Jangan pernah menerapkan aturan koding, kerangka kerja (framework), atau standar basis data dari satu proyek ke proyek lainnya.
- **Project-Specific Knowledge**: Saat pengguna meminta Anda mengerjakan sebuah sub-proyek (misalnya **SILATRASA** di `outputs/silatrasa/`), Anda **WAJIB membaca pedoman khusus** yang ada di folder proyek tersebut (misalnya `outputs/silatrasa/project-knowledge.md` atau `outputs/silatrasa/documents/development_history.md`) sebelum mulai mengode.

## 2. Proactive Knowledge Extraction (Pengingat Otomatis)
Karena pengguna (Human) mungkin lupa kapan harus menginstruksikan penyimpanan *knowledge*, **Anda sebagai AI Agent WAJIB bertindak proaktif.**
Setiap kali Anda:
- Berhasil memecahkan *bug* yang kompleks.
- Menetapkan pola desain (Design Pattern) atau struktur baru bersama pengguna.
- Menemukan batasan/quirks pada kerangka kerja (framework) yang sedang dipakai.
**Tugas Anda:** Anda WAJIB menawarkan kepada pengguna untuk menyimpan penemuan tersebut secara permanen. (Contoh: *"Masalah ini sudah selesai. Apakah Anda ingin saya otomatis menyimpan pola penyelesaian ini ke berkas aturan spesifik proyek Anda?"* atau ingatkan mereka untuk memakai perintah `/learn`).

## 3. Catatan Pengembangan (Improvement Backlog)
Jika pengguna meminta Anda untuk meninjau atau menambahkan ide pengembangan masa depan untuk AI-SEOS, satu-satunya berkas yang boleh Anda sentuh/baca adalah: **`meta/improvement-backlog.md`**. Dilarang mengimplementasikan draf di dalam berkas tersebut sebelum ada instruksi eksplisit dari pengguna.

## 4. Aturan Koding Khusus Proyek (Contoh: SILATRASA)
*(Aturan spesifik untuk proyek SILATRASA seperti keharusan menggunakan SQLite In-Memory, Http::fake(), definisi tabel `feedbacks`, dan struktur `outputs/silatrasa/silatrasa-app/` kini diisolasi sepenuhnya di foldernya masing-masing. Agen AI dilarang memberlakukan aturan SILATRASA pada proyek lain dalam repositori ini).*
