# KREKI Enterprise Architecture Standards

**TOGAF 9.2-based Emergency Services Framework for Indonesia**

This repository contains the **Enterprise Architecture (EA) standards and reference framework** for KREKI (Komunitas Relawan Emergensi Kesehatan Indonesia) - Indonesia's national reference for emergency services digital infrastructure.

## 📖 About This Repository

This is the **standards repository** of the kreki-indonesia GitHub organization. It provides:

- **TOGAF 9.2-based EA framework** customized for emergency services
- **Reference architecture** for emergency response systems
- **Technical standards** for FHIR integration, security, and interoperability
- **Implementation guidelines** for organizations adopting KREKI standards

### License

**CC BY 4.0** - This repository is open source. You are free to use, adapt, and build upon these standards with attribution.

---

## 🌐 KREKI Indonesia Organization

This repository is part of the **kreki-indonesia** GitHub organization, which includes:

| Repository | Purpose | License |
|------------|---------|---------|
| **ea-standards** (this repo) | Enterprise Architecture framework | CC BY 4.0 |
| [api-specifications](https://github.com/kreki-indonesia/api-specifications) | OpenAPI specifications | MIT |
| [fhir-profiles](https://github.com/kreki-indonesia/fhir-profiles) | FHIR implementation guides | Apache 2.0 |
| [security-framework](https://github.com/kreki-indonesia/security-framework) | Zero Trust security standards | MIT |
| [certification-framework](https://github.com/kreki-indonesia/certification-framework) | Certification programs | CC BY 4.0 |

**Platform Services:**
- [help-119-mobile](https://github.com/kreki-indonesia/help-119-mobile) - Mobile application
- [help-119-backend](https://github.com/kreki-indonesia/help-119-backend) - Backend services
- [kreki-auth-service](https://github.com/kreki-indonesia/kreki-auth-service) - Authentication
- [kreki-emergency-core](https://github.com/kreki-indonesia/kreki-emergency-core) - Geo-dispatch engine
- [kreki-lms](https://github.com/kreki-indonesia/kreki-lms) - Learning platform
- [satusehat-bridge](https://github.com/kreki-indonesia/satusehat-bridge) - SATUSEHAT integration

---

## 📁 Documentation Structure

```
ea-standards/
├── README.md                    # This file
├── LICENSE                      # CC BY 4.0
├── GOVERNANCE.md                # Governance structure
├── CONTRIBUTING.md              # Contribution guidelines
└── docs/                        # EA documentation
    ├── README.md                # Documentation overview
    ├── index.md                 # Main index (Indonesian)
    ├── business-architecture.md # Business Architecture
    ├── data-architecture.md     # Data Architecture
    ├── application-architecture.md # Application Architecture
    ├── technology-architecture.md # Technology Architecture
    ├── security-architecture.md # Security Architecture
    ├── integration-architecture.md # Integration Architecture
    ├── ea-governance.md         # EA Governance
    ├── roadmap.md               # EA Roadmap
    └── [30+ more documents]
```

---

## 🚀 Quick Start

### For Enterprise Architects

1. Read the [EA Governance](docs/ea-governance.md) to understand the framework
2. Review [Architecture Domains](docs/README.md#core-enterprise-architecture-togaf-92)
3. Study the [Roadmap](docs/roadmap.md) for evolution phases

### For System Architects

1. Start with [System Architecture](docs/system-architecture.md)
2. Review [Integration Architecture](docs/integration-architecture.md) for FHIR/SATUSEHAT
3. Study [Security Architecture](docs/security-architecture.md) for Zero Trust

### For Organizations Adopting KREKI Standards

1. Read [Business Architecture](docs/business-architecture.md) for capabilities
2. Review [Technology Architecture](docs/technology-architecture.md) for stack
3. Follow [Contribution Guidelines](CONTRIBUTING.md) for engagement

---

## 🏗️ Enterprise Architecture Framework

### TOGAF 9.2 Customization

KREKI's EA framework is based on **TOGAF 9.2** with customization for Indonesian emergency services:

- **Phase A**: Emergency response outcomes (survival rate, response time)
- **Phase B**: Emergency capabilities (panic button, dispatch, volunteer coordination)
- **Phase C-D**: FHIR-based healthcare data exchange
- **Phase E**: Cloud-native, mobile-first infrastructure
- **Phase F**: Pilot → Regional → National rollout

### Architecture Domains

| Domain | Description | Document |
|--------|-------------|----------|
| Business | Capabilities, value streams, stakeholder map | [→](docs/business-architecture.md) |
| Data | Data domains, FHIR integration, governance | [→](docs/data-architecture.md) |
| Application | Portfolio, lifecycle, microservices | [→](docs/application-architecture.md) |
| Technology | Stack, infrastructure, standards | [→](docs/technology-architecture.md) |
| Security | Zero Trust, PDP Law 2022 compliance | [→](docs/security-architecture.md) |
| Integration | FHIR R4, SATUSEHAT, API patterns | [→](docs/integration-architecture.md) |

---

## 🔗 Key Standards

### Healthcare Integration

- **FHIR R4**: Primary standard for healthcare data exchange
- **SATUSEHAT**: Indonesia's national health data platform
- **PostGIS**: Geospatial data for volunteer matching

### Security & Compliance

- **Zero Trust Architecture**: Never trust, always verify
- **PDP Law 2022**: Indonesian data protection compliance
- **OAuth 2.0 / JWT**: Authentication and authorization

### Technology Stack

- **Backend**: Node.js 20.x, Go 1.21+
- **Mobile**: React Native 0.73+
- **Database**: PostgreSQL 15+ with PostGIS
- **Infrastructure**: Docker 24+, Kubernetes
- **API**: RESTful with OpenAPI 3.0 specification

---

## 🤝 Contributing

This is an open source repository. We welcome contributions!

### Contribution Process

1. Read [CONTRIBUTING.md](CONTRIBUTING.md)
2. Fork the repository
3. Create a branch for your changes
4. Submit a Pull Request

### Standards Change Process

For significant changes to EA standards:

1. Submit an RFC (Request for Comments) via GitHub Issues
2. Technical Committee review (monthly meetings)
3. Public comment period (3 weeks)
4. Approval by Technical Board (2/3 majority)
5. Publication in this repository

See [EA Governance](docs/ea-governance.md) for details.

---

## 📞 Support & Contact

### For Standards Adoption

- **Email**: dev-support@kreki.or.id
- **GitHub Issues**: Report bugs or request features
- **Discussions**: Ask questions and engage with community

### For Security Issues

- **Email**: security@kreki.or.id
- Please do NOT open public issues for security vulnerabilities

### General Inquiries

- **Website**: https://kreki.id
- **Email**: sekretariat.kreki@gmail.com

---

## 📜 License

This repository is licensed under **Creative Commons Attribution 4.0 International (CC BY 4.0)**.

You are free to:
- **Share** - Copy and redistribute the material
- **Adapt** - Remix, transform, and build upon the material

Under the following terms:
- **Attribution** - You must give appropriate credit to KREKI

For full license text, see [LICENSE](LICENSE).

---

## 🌟 Acknowledgments

This EA framework is developed by KREKI (Komunitas Relawan Emergensi Kesehatan Indonesia) in collaboration with:

- **Kemenkes** (Indonesian Ministry of Health)
- **PSC 119** (Public Safety Center)
- **Healthcare professionals** across Indonesia
- **Open source community**

---

**Organization**: [KREKI Indonesia](https://github.com/kreki-indonesia)
**Website**: https://kreki.id
**Last Updated**: 2026-01-10
**Version**: 2.0.0
