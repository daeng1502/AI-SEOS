# Context Builder

Version: 1.0
Status: Final

---

# Purpose

Context Builder bertanggung jawab menyusun Context yang relevan dari Knowledge untuk mendukung pelaksanaan Task sesuai Workflow.

Context Builder tidak menghasilkan Engineering Artifact.

---

# Principles

- Knowledge Driven
- Relevant
- Minimal
- Traceable
- Consistent

---

# Responsibilities

Context Builder bertanggung jawab untuk:

- memilih Knowledge yang relevan;
- menyusun Context sesuai Task;
- menjaga konsistensi Context;
- memastikan Context dapat ditelusuri ke sumber Knowledge.

---

# Context Building Flow

Knowledge

↓

Context Selection

↓

Context Organization

↓

Context Validation

↓

Task Context

---

# Rules

- Context hanya menggunakan Knowledge yang valid.
- Context hanya memuat informasi yang relevan.
- Context harus dapat ditelusuri ke sumber Knowledge.
- Context tidak boleh mengubah Knowledge.

---

# Inputs

- Knowledge
- Workflow
- Task

---

# Outputs

- Context

---

# Constraints

Context Builder bersifat konseptual.

Context Builder tidak mendefinisikan mekanisme implementasi Context pada AI Orchestrator.

---

# Version History

| Version | Description |
|----------|-------------|
| 1.0 | Initial Context Builder |