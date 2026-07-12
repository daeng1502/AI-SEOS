# Role Engine

Version: 1.0
Status: Final

---

# Purpose

Role Engine bertanggung jawab menentukan Role yang bertanggung jawab terhadap setiap Task berdasarkan Workflow dan struktur Team.

Role Engine tidak menjalankan Role maupun menghasilkan Engineering Artifact.

---

# Principles

- Responsibility Driven
- Traceable
- Consistent
- Standardized
- Technology Agnostic

---

# Responsibilities

Role Engine bertanggung jawab untuk:

- mengidentifikasi Role yang sesuai;
- menghubungkan Role dengan Task;
- memastikan setiap Task memiliki Role utama;
- menjaga konsistensi pembagian tanggung jawab.

---

# Role Assignment Flow

Workflow

↓

Task

↓

Role Identification

↓

Role Assignment

↓

Task Responsibility

---

# Rules

- Setiap Task memiliki satu Role utama.
- Satu Role dapat menangani lebih dari satu Task.
- Penugasan Role mengikuti Workflow.
- Role tidak boleh bertentangan dengan definisi pada ROLES.md.

---

# Inputs

- Workflow
- Tasks
- Roles

---

# Outputs

- Role Assignment

---

# Constraints

Role Engine bersifat konseptual.

Role Engine tidak mendefinisikan implementasi AI Agent maupun AI Orchestrator.

---

# Version History

| Version | Description |
|----------|-------------|
| 1.0 | Initial Role Engine |