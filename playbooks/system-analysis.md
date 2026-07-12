# System Analysis Playbook

Version: 1.0
Status: Final

---

# Purpose

Playbook ini mendefinisikan langkah-langkah untuk menganalisis sistem berdasarkan Requirement yang telah divalidasi sehingga menghasilkan model sistem yang konsisten.

---

# Objective

- Memahami perilaku sistem.
- Mengidentifikasi aktor dan proses.
- Mengidentifikasi objek dan relasi.
- Menyiapkan dasar untuk Software Architecture.

---

# Inputs

- Validated Requirement Specification
- Business Rules
- Business Process
- Domain Knowledge

---

# Outputs

- Use Case Model
- BPMN (Business Process Model and Notation)
- Activity Diagram
- Sequence Diagram
- Class Diagram
- Domain Analysis Report

---

# Execution Steps

1. Review Requirement Specification.
2. Identifikasi Actor.
3. Identifikasi Use Case.
4. Identifikasi Business Process.
5. Susun diagram proses bisnis (BPMN) dengan membagi menjadi proses berjalan (As-Is), proses usulan (To-Be), serta menyusun tabel analisis kesenjangan (Gap Analysis).
6. Susun Activity Diagram.
7. Susun Sequence Diagram.
8. Identifikasi Entity dan Object.
9. Susun Class Diagram.
10. Verifikasi konsistensi antar model.
11. Dokumentasikan hasil analisis.

---

# Analysis Checklist

- Seluruh Actor telah teridentifikasi.
- Seluruh Use Case berasal dari Requirement.
- BPMN sesuai dengan proses bisnis aktual dan usulan.
- Activity Diagram sesuai proses bisnis.
- Sequence Diagram sesuai Use Case.
- Class Diagram konsisten dengan Domain Model.
- **Kepatuhan Asumsi Nihil**: Seluruh model analisis dan proses bisnis (BPMN) tidak memuat detail informal atau spekulatif yang tidak tercantum di `project-knowledge.md` (Sesuai `[RULE-HITL-001]`).

---

# Completion Criteria

- Seluruh model sistem dan proses bisnis (BPMN) selesai.
- Tidak terdapat konflik antar diagram.
- Seluruh model dapat ditelusuri ke Requirement.

---

# Deliverables

- Use Case Diagram
- BPMN Document
- Activity Diagram
- Sequence Diagram
- Class Diagram
- System Analysis Report

---

# References

- requirement-validation.md
- uml-modeling.md
- bpmn-template.md
- DOMAIN_MODEL.md

---

# Version History

| Version | Description |
|----------|-------------|
| 1.0 | Initial System Analysis Playbook |
| 1.1 | Integrasi BPMN ke dalam Output, Langkah Eksekusi, dan Deliverables |
| 1.2 | Standardisasi pemisahan proses bisnis As-Is/To-Be dan penulisan Gap Analysis pada pemodelan BPMN |
| 1.3 | Standardisasi aturan Kepatuhan Asumsi Nihil (RULE-HITL-001) pada checklist analisis |