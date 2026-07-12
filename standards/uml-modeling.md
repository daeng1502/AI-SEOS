# UML Modeling Standard

Version: 1.0
Status: Final

---

# Purpose

Standar ini mendefinisikan aturan pemodelan UML agar seluruh diagram memiliki struktur yang konsisten, mudah dipahami, dan dapat ditelusuri kembali ke Requirement.

---

# Objective

- Menstandarkan penggunaan UML.
- Memastikan setiap diagram memiliki tujuan yang jelas.
- Menjaga konsistensi antar diagram.
- Mendukung traceability Requirement → Design.

---

# Supported UML Diagrams

- Use Case Diagram
- Activity Diagram
- Sequence Diagram
- Class Diagram

---

# Inputs

- Functional Requirements
- Software Architecture
- Business Process

---

# Outputs

- UML Diagrams
- UML Description

---

# Modeling Process

1. Review Requirements
2. Select Diagram Type
3. Define Elements
4. Define Relationships
5. Validate Consistency
6. Review Diagram
7. Approve Diagram

---

# General Rules

Seluruh UML Diagram harus:

- memiliki judul;
- memiliki tujuan;
- menggunakan notasi UML standar;
- konsisten dengan Requirement;
- konsisten dengan diagram lainnya.

---

# Use Case Rules

- Setiap Actor berasal dari Requirement.
- Setiap Use Case memiliki tujuan bisnis.
- Gunakan <<include>> dan <<extend>> hanya bila diperlukan.

---

# Activity Diagram Rules

- Memiliki Initial Node dan Final Node.
- Menggunakan Decision dan Merge sesuai kebutuhan.
- Menggambarkan alur proses bisnis.

---

# Sequence Diagram Rules

- Menggunakan Lifeline yang jelas.
- Menunjukkan urutan interaksi.
- Tidak menambahkan objek yang tidak berasal dari Requirement.

---

# Class Diagram Rules

- Setiap Class memiliki nama yang jelas.
- Relationship menggunakan notasi UML standar.
- Attribute dan Operation sesuai kebutuhan sistem.

---

# UML Quality Checklist

- Complete
- Consistent
- Correct
- Readable
- Traceable
- Standardized

---

# Deliverables

- Use Case Diagram
- Activity Diagram
- Sequence Diagram
- Class Diagram

---

# References

- requirement-analysis.md
- software-architecture.md

---

# Version History

| Version | Description |
|----------|-------------|
| 1.0 | Initial UML Modeling Standard |