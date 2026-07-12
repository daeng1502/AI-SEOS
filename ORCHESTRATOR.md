# Orchestrator

Version: 1.0
Status: Final

---

# Purpose

Orchestrator bertanggung jawab mengoordinasikan seluruh komponen AI-SEOS agar proses software engineering berjalan sesuai Workflow.

Orchestrator tidak menghasilkan Artifact.

---

# Principles

- Coordination First
- Workflow Driven
- Traceable
- Deterministic
- Technology Agnostic

---

# Responsibilities

Orchestrator bertanggung jawab untuk:

- memulai proses Project;
- mengelola urutan Workflow;
- mengoordinasikan Project Planner;
- mengoordinasikan Team Builder;
- mengoordinasikan Context Builder;
- mengoordinasikan Role Engine;
- mengoordinasikan Skill Engine;
- memastikan setiap Task selesai sebelum melanjutkan ke tahap berikutnya.

---

# Orchestration Flow

Project

↓

Project Planner

↓

Team Builder

↓

Context Builder

↓

Role Engine

↓

Skill Engine

↓

Artifact

---

# Rules

- Seluruh proses mengikuti Workflow.
- Tidak boleh melewati tahapan.
- Seluruh keputusan harus dapat ditelusuri.
- Setiap Artifact harus memiliki sumber Knowledge.

---

# Inputs

- Project
- Knowledge
- Workflow

---

# Outputs

- Coordinated Engineering Process

---

# Constraints

Orchestrator tidak:

- menghasilkan Artifact;
- mengubah Knowledge;
- mengubah Workflow.

---

# Version History

| Version | Description |
|----------|-------------|
| 1.0 | Initial Orchestrator |