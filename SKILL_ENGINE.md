# Skill Engine

Version: 1.0
Status: Final

---

# Purpose

Skill Engine bertanggung jawab menentukan Skill yang diperlukan untuk menyelesaikan setiap Task berdasarkan Role dan Workflow.

Skill Engine tidak menjalankan Skill maupun menghasilkan Engineering Artifact.

---

# Principles

- Capability Driven
- Traceable
- Consistent
- Reusable
- Technology Agnostic

---

# Responsibilities

Skill Engine bertanggung jawab untuk:

- mengidentifikasi Skill yang diperlukan;
- menghubungkan Skill dengan Role;
- memastikan setiap Task memiliki Skill yang sesuai;
- menjaga konsistensi penggunaan Skill.

---

# Skill Assignment Flow

Workflow

↓

Task

↓

Role

↓

Skill Identification

↓

Skill Assignment

---

# Rules

- Setiap Task memiliki minimal satu Skill.
- Satu Skill dapat digunakan oleh banyak Role.
- Pemilihan Skill mengikuti Workflow.
- Skill harus sesuai dengan definisi pada SKILLS.md.

---

# Inputs

- Workflow
- Tasks
- Roles
- Skills

---

# Outputs

- Skill Assignment

---

# Constraints

Skill Engine bersifat konseptual.

Skill Engine tidak mendefinisikan implementasi AI Agent maupun AI Orchestrator.

---

# Version History

| Version | Description |
|----------|-------------|
| 1.0 | Initial Skill Engine |