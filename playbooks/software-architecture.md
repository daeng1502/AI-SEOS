# Software Architecture Playbook

Version: 1.0
Status: Final

---

# Purpose

Playbook ini mendefinisikan langkah-langkah untuk merancang arsitektur perangkat lunak berdasarkan hasil analisis sistem dan Requirement yang telah divalidasi.

---

# Objective

- Menentukan struktur sistem.
- Menentukan komponen utama.
- Menentukan hubungan antar komponen.
- Menghasilkan arsitektur yang mudah dipelihara dan dikembangkan.

---

# Inputs

- Validated Requirement Specification
- System Analysis Report
- Domain Model
- Non-Functional Requirements

---

# Outputs

- Software Architecture Document
- Component Diagram
- Architecture Decision Record
- Technology Stack Recommendation

---

# Execution Steps

1. Review Requirement Specification.
2. Review hasil System Analysis.
3. Identifikasi komponen sistem.
4. Tentukan tanggung jawab setiap komponen.
5. Tentukan hubungan antar komponen.
6. Tentukan pola arsitektur yang sesuai.
7. Tentukan strategi penyimpanan data.
8. Tentukan integrasi eksternal.
9. Review arsitektur.
10. Dokumentasikan hasil arsitektur.

---

# Architecture Checklist

- Seluruh Requirement memiliki solusi arsitektur.
- Tidak terdapat duplikasi tanggung jawab.
- Komponen memiliki batas yang jelas.
- Arsitektur mendukung scalability.
- Arsitektur mendukung maintainability.
- Arsitektur dapat ditelusuri ke Requirement.
- **Kepatuhan Asumsi Nihil**: Seluruh keputusan arsitektur (ADR) dan dokumen arsitektur (SAD) tidak memuat batasan teknis atau infrastruktur di luar apa yang didefinisikan dalam `project-knowledge.md` (Sesuai `[RULE-HITL-005]`).

---

# Completion Criteria

- Software Architecture selesai.
- Component Diagram selesai.
- Architecture Decision terdokumentasi.
- Architecture telah direview.

---

# Deliverables

- Software Architecture Document
- Component Diagram
- Architecture Decision Record

---

# References

- software-architecture.md (Standard)
- sad-template.md
- adr-template.md
- system-analysis.md
- DOMAIN_MODEL.md

---

# Version History

| Version | Description |
|----------|-------------|
| 1.0 | Initial Software Architecture Playbook |
| 1.1 | Menambahkan referensi sad-template.md dan adr-template.md |
| 1.2 | Standardisasi aturan Kepatuhan Asumsi Nihil (RULE-HITL-005) pada checklist arsitektur |