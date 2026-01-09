---
title: "Dokumentasi KREKI"
description: "Pusat dokumentasi sistem informasi dan tata kelola KREKI"
category: "index"
last_updated: 2026-01-10
---

# Dokumentasi KREKI

Selamat datang di dokumentasi resmi **Komunitas Relawan Emergensi Kesehatan Indonesia (KREKI)**. Dokumentasi ini berisi blueprints, standar tata kelola, dan peta jalan teknologi untuk seluruh inisiatif digital KREKI.

##  Mulai Cepat

| Untuk Anda | Mulai Dari |
|-----------|------------|
| **Developer Baru** | [Panduan Kontribusi](contribution-guide.md) |
| **Architect/Lead** | [Enterprise Architecture](architecture-domains/) |
| **Ops/DevOps** | [Tata Kelola IT](it-governance.md) |
| **General Info** | [Tentang KREKI](organization.md) |

## Kategori Dokumentasi

###  Governance

Framework tata kelola IT, Service Level Objectives (SLOs), incident management, dan operational procedures.

- [Tata Kelola Sistem Informasi](it-governance.md) - Framework governance lengkap
- [SLA & SLO Definition](sla-slo.md) - Service level agreements dan objectives
- [Incident Management](incident-management.md) - Prosedur respon insiden

###  Architecture

Desain teknis microservices, teknologi stack, dan deployment strategy.

- [System Architecture](system-architecture.md) - Desain arsitektur lengkap
- [Microservices Design](microservices-design.md) - Detail microservices

###  Contributing

Panduan kontribusi untuk developer, standar kode, dan Git workflow.

- [Contribution Guide](contribution-guide.md) - Cara berkontribusi
- [Code Review Standards](code-review-standards.md) - Standar review kode

###  About

Informasi organisasi, kontak, dan program KREKI.

- [Organization Profile](organization.md) - Profil lengkap organisasi
- [Contact & Partners](contact.md) - Kontak dan mitra strategis

###  Manual / Panduan

Panduan pengguna untuk aplikasi dan layanan KREKI.

- [Panduan HELP 119](https://github.com/KREKI-indonesia/docs-portal/blob/main/help-119-guide.md) - Panduan lengkap penggunaan aplikasi HELP 119 untuk masyarakat dan relawan

###  Enterprise Architecture

Enterprise Architecture (EA) framework sebagai "rumah tumbuh" untuk ekosistem digital KREKI.

- [EA Overview](#enterprise-architecture) - Dokumentasi EA di direktori docs ini
- [Business Architecture](business-architecture.md) - Kapabilitas bisnis, value streams, stakeholder
- [Data Architecture](data-architecture.md) - Data domains, flows, governance
- [Application Architecture](application-architecture.md) - Portfolio aplikasi dan lifecycle
- [Technology Architecture](technology-architecture.md) - Technology stack dan standards
- [Security Architecture](security-architecture.md) - Security domains dan controls
- [Integration Architecture](integration-architecture.md) - Integration patterns dan standards
- [Innovation Framework](innovation-framework.md) - Technology radar dan emerging tech
- [EA Governance](ea-governance.md) - Tata kelola EA dan update cycle
- [EA Roadmap](roadmap.md) - Peta jalan evolusi EA

###  Engineering

Technical handbook untuk ekosistem digital KREKI.

- [Engineering Handbook](handbook.md) - Technical handbook

## Struktur Folder

```
ea-standards/
├── README.md                      # Entry point repositori
├── LICENSE                        # CC BY 4.0 License
├── GOVERNANCE.md                  # Governance structure
├── CONTRIBUTING.md                # Contribution guidelines
└── docs/                          # Dokumentasi utama
    ├── README.md                  # Documentation overview
    ├── index.md                   # Index halaman ini
    ├── business-architecture.md   # Business Architecture
    ├── data-architecture.md       # Data Architecture
    ├── application-architecture.md # Application Architecture
    ├── technology-architecture.md # Technology Architecture
    ├── security-architecture.md   # Security Architecture
    ├── integration-architecture.md # Integration Architecture
    ├── ea-governance.md           # EA Governance
    ├── roadmap.md                 # EA Roadmap
    ├── innovation-framework.md    # Innovation Framework
    ├── compliance/                # Compliance documentation (planned)
    ├── patterns/                  # Architecture patterns (planned)
    └── [various docs].md          # Individual documentation files
```

## Kontribusi

Dokumentasi ini bersifat open dan kolaboratif. Untuk berkontribusi:

1. Baca [Contribution Guide](contribution-guide.md)
2. Fork repositori
3. Buat branch untuk perubahan
4. Submit Pull Request

## Dukungan

Untuk pertanyaan atau dukungan:

- **Email:** it-support@KREKI.or.id
- **Security Issues:** security@KREKI.or.id
- **General:** sekretariat.KREKI@gmail.com

---

*Terdapat di [KREKI.id](https://KREKI.id) | [GitHub](https://github.com/KREKI-indonesia)*
