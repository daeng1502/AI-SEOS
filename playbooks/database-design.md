# Database Design Playbook

Version: 1.0
Status: Final

---

# Purpose

Playbook ini mendefinisikan langkah-langkah untuk merancang basis data berdasarkan Requirement dan hasil analisis sistem sehingga menghasilkan struktur data yang konsisten, terintegrasi, dan mudah dipelihara.

---

# Objective

- Mengidentifikasi Entity.
- Menentukan Attribute.
- Menentukan Relationship.
- Menghasilkan database yang terstruktur dan ternormalisasi.

---

# Inputs

- Validated Requirement Specification
- System Analysis Report
- Domain Model
- Software Architecture

---

# Outputs

- Entity Relationship Diagram (ERD)
- Database Schema
- Data Dictionary

---

# Execution Steps

1. Review Requirement Specification.
2. Identifikasi Entity.
3. Identifikasi Attribute.
4. Tentukan Primary Key.
5. Tentukan Foreign Key.
6. Tentukan Relationship.
7. Lakukan Normalization.
8. Validasi desain database.
9. Review hasil desain.
10. Dokumentasikan database.

---

# Database Checklist

- Seluruh Entity berasal dari Requirement.
- Setiap Entity memiliki Primary Key.
- Relationship telah didefinisikan.
- Database memenuhi minimal Third Normal Form (3NF).
- Tidak terdapat redundansi yang tidak diperlukan.
- Seluruh tabel memiliki deskripsi.

---

# Completion Criteria

- ERD selesai.
- Database Schema selesai.
- Data Dictionary selesai.
- Desain database telah direview.

---

# Deliverables

- Entity Relationship Diagram
- Database Schema
- Data Dictionary

---

# References

- database-design.md (Standard)
- software-architecture.md
- system-analysis.md

---

# Version History

| Version | Description |
|----------|-------------|
| 1.0 | Initial Database Design Playbook |