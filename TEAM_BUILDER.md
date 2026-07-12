# Team Builder

Version: 1.0
Status: Final

---

# Purpose

Team Builder bertanggung jawab menentukan Role yang diperlukan untuk setiap Project berdasarkan Knowledge, Workflow, dan Task.

Team Builder tidak membentuk AI Agent maupun mengimplementasikan mekanisme eksekusi.

---

# Principles

- Requirement Driven
- Role Based
- Traceable
- Reusable
- Standardized

---

# Responsibilities

Team Builder bertanggung jawab untuk:

- menganalisis kebutuhan Project;
- mengidentifikasi Role yang diperlukan;
- menyusun struktur Team;
- memastikan setiap Task memiliki Role yang bertanggung jawab.

---

# Team Building Flow

Project

↓

Knowledge

↓

Workflow

↓

Tasks

↓

Required Roles

↓

Engineering Team

---

# Rules

- Setiap Task harus memiliki minimal satu Role.
- Satu Role dapat menangani lebih dari satu Task.
- Struktur Team disusun sebelum Project dimulai.
- Team harus mengikuti Workflow yang telah ditetapkan.

---

# Inputs

- Project
- Knowledge
- Workflow
- Tasks

---

# Outputs

- Team Structure
- Role Assignment

---

# Constraints

Team Builder tidak:

- menjalankan Task;
- menghasilkan Artifact;
- mengubah Knowledge.

---

# Version History

| Version | Description |
|----------|-------------|
| 1.0 | Initial Team Builder |