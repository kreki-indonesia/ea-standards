# KREKI Emergency Services Enterprise Architecture Standards

**National Reference Standards for Indonesia's Emergency Services Ecosystem**

---

## Overview

This repository contains the **KREKI Emergency Services Enterprise Architecture (EA) Standards** - a comprehensive framework based on TOGAF 9.2, customized for Indonesia's emergency response and healthcare ecosystem.

These standards are designed to be **adopted by any emergency services organization** in Indonesia, including hospitals, PSC 119 centers, volunteer organizations, and government agencies.

## License

**Creative Commons Attribution 4.0 International (CC BY 4.0)**

You are free to:
- **Share**: Copy and redistribute the material in any medium or format
- **Adapt**: Remix, transform, and build upon the material

Under the following terms:
- **Attribution**: You must give appropriate credit to KREKI, provide a link to the license, and indicate if changes were made.

## Purpose

These standards provide:

1. **Reference Architecture**: Proven patterns for emergency services digital systems
2. **Best Practices**: Lessons learned from KREKI's implementation since 2018
3. **Integration Standards**: FHIR, SATUSEHAT, and national healthcare system integration
4. **Governance Framework**: IT governance and operational guidelines
5. **Compliance Guidelines**: Kemenkes, UU PDP 2022, and international standards alignment

## Who Should Use These Standards

- **Emergency Response Organizations**: PMI, BASARNAS, hospital emergency departments
- **Government Agencies**: PSC 119, Dinas Kesehatan, BPBD
- **Healthcare Providers**: Hospitals, clinics, health centers
- **Volunteer Organizations**: Community emergency response groups
- **Technology Partners**: Software vendors, system integrators

## Document Structure

```
ea-standards/
├── README.md                    # This file
├── docs/
│   ├── overview.md              # What is emergency services EA
│   ├── adoption-guide.md        # How to adopt in your organization
│   ├── architecture-domains/
│   │   ├── business-architecture.md
│   │   ├── data-architecture.md
│   │   ├── application-architecture.md
│   │   ├── technology-architecture.md
│   │   ├── security-architecture.md
│   │   └── integration-architecture.md
│   ├── patterns/                # Reference patterns
│   │   ├── geo-dispatch.md
│   │   ├── volunteer-matching.md
│   │   └── fhir-integration.md
│   └── compliance/              # Compliance checklists
│       ├── kemenkes-compliance.md
│       └── pdp-law-compliance.md
├── examples/                    # Example implementations
│   ├── hospital-emergency-system/
│   └── regional-emergency-center/
└── tools/
    ├── compliance-checker.py
    └── maturity-assessment.md
```

## Quick Start

### 1. Review the Standards

Start with the [Overview](docs/overview.md) to understand the framework.

### 2. Assess Your Organization

Use the [Maturity Assessment Tool](tools/maturity-assessment.md) to evaluate your current state.

### 3. Plan Your Adoption

Follow the [Adoption Guide](docs/adoption-guide.md) for a step-by-step implementation plan.

### 4. Validate Compliance

Use the [Compliance Checker](tools/compliance-checker.py) to verify your implementation.

## Architecture Domains

### Business Architecture
Defines emergency response capabilities, value streams, and organizational structures.

**Key Documents:**
- [Business Capability Map](docs/architecture-domains/business-architecture.md)
- Emergency Response Workflows
- Volunteer Management Framework
- Stakeholder Integration Patterns

### Data Architecture
Defines data domains, governance, and privacy requirements.

**Key Documents:**
- [Data Domain Model](docs/architecture-domains/data-architecture.md)
- FHIR R4 Implementation Guides
- UU PDP 2022 Compliance
- Data Privacy and Security

### Application Architecture
Defines application portfolio and integration patterns.

**Key Documents:**
- [Application Landscape](docs/architecture-domains/application-architecture.md)
- Microservices Design Patterns
- API Design Standards
- Integration with SATUSEHAT

### Technology Architecture
Defines technology stack and infrastructure standards.

**Key Documents:**
- [Technology Reference Model](docs/architecture-domains/technology-architecture.md)
- Cloud-Native Infrastructure
- Mobile-First Architecture
- High Availability and Resilience

### Security Architecture
Defines security domains and controls.

**Key Documents:**
- [Zero Trust Framework](docs/architecture-domains/security-architecture.md)
- Identity and Access Management
- Data Encryption Standards
- Incident Response Procedures

### Integration Architecture
Defines integration patterns and standards.

**Key Documents:**
- [FHIR Integration](docs/architecture-domains/integration-architecture.md)
- PSC 119 Integration
- SATUSEHAT Integration
- API Gateway Patterns

## Reference Patterns

### Geo-Dispatch Algorithm
Reference implementation for finding nearest available volunteers.

**Location:** [docs/patterns/geo-dispatch.md](docs/patterns/geo-dispatch.md)

### Volunteer Matching
Best practices for matching volunteers to emergencies based on skills, location, and availability.

**Location:** [docs/patterns/volunteer-matching.md](docs/patterns/volunteer-matching.md)

### FHIR Integration
Implementation guides for FHIR R4 resources in emergency response.

**Location:** [docs/patterns/fhir-integration.md](docs/patterns/fhir-integration.md)

## Compliance Framework

### Kemenkes Compliance
Ensure alignment with Ministry of Health regulations.

**Location:** [docs/compliance/kemenkes-compliance.md](docs/compliance/kemenkes-compliance.md)

### UU PDP 2022 Compliance
Personal Data Protection Law compliance for emergency services.

**Location:** [docs/compliance/pdp-law-compliance.md](docs/compliance/pdp-law-compliance.md)

## Certification Levels

KREKI offers three certification levels for organizations adopting these standards:

### Level 1: Standards Compliant (Free)
- Self-assessment using compliance checker
- Can claim "Follows KREKI Standards"
- No formal endorsement

### Level 2: Certified Implementation (Fee)
- Formal audit by KREKI team
- Can use "KREKI Certified" badge
- Listed in KREKI certified directory
- Annual re-certification required

### Level 3: Licensed Platform (License Fee)
- Full KREKI platform deployment
- "Powered by KREKI Platform"
- Official partner status
- Priority support

For certification details, visit: https://kreki.or.id/certification

## Contributing

We welcome contributions to these standards!

### How to Contribute

1. Fork this repository
2. Create a branch for your standard/proposal
3. Draft your standard following our [Template](.github/STANDARD_TEMPLATE.md)
4. Submit a Pull Request

### Standards Development Process

1. **Proposal Phase** (3 months): Identify gap, draft specification
2. **Development Phase** (6 months): Working group review
3. **Public Review Phase** (3 months): Public comment period
4. **Approval Phase** (1 month): Technical Board vote
5. **Publication**: Standard published

For more details, see [CONTRIBUTING.md](CONTRIBUTING.md)

## Governance

### Technical Committee
- Approves all standards before publication
- Meets monthly
- 2/3 majority vote required for approval

### Standards Oversight Committee
- Manages standards development process
- Reviews and approves proposals
- Ensures stakeholder representation
- Meets quarterly

For governance details, see: https://github.com/kreki-indonesia/governance

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0.0 | 2025-01-09 | Initial publication based on KREKI EA framework |

## Support

### Documentation
- Full documentation: https://docs.kreki.id/ea-standards
- Adoption guide: https://docs.kreki.id/ea-standards/adoption
- Video tutorials: https://learn.kreki.id

### Community
- GitHub Discussions: https://github.com/kreki-indonesia/ea-standards/discussions
- Slack Community: https://kreki-indonesia.slack.com
- Monthly Office Hours: Last Thursday of each month

### Professional Support
- Email: standards-support@kreki.or.id
- Consulting: services@kreki.or.id
- Training: training@kreki.or.id

## Citation

If you use these standards in your organization or research, please cite:

```bibtex
@misc{kreki-ea-standards-2025,
  title={KREKI Emergency Services Enterprise Architecture Standards},
  author={{KREKI Technical Committee}},
  year={2025},
  publisher={Komunitas Relawan Emergensi Kesehatan Indonesia},
  url={https://github.com/kreki-indonesia/ea-standards}
}
```

## Acknowledgments

These standards were developed by KREKI (Komunitas Relawan Emergensi Kesehatan Indonesia) based on:

- **TOGAF 9.2** (The Open Group)
- **FHIR R4** (HL7 International)
- **Indonesia National Health IT Standards** (Kemenkes)
- **Emergency Response Best Practices** (WHO, IFRC)

## License Details

```
Creative Commons Attribution 4.0 International

Copyright (c) 2025 Komunitas Relawan Emergensi Kesehatan Indonesia (KREKI)

You are free to:
- Share — copy and redistribute the material in any medium or format
- Adapt — remix, transform, and build upon the material

Under the following terms:
- Attribution — You must give appropriate credit to KREKI, provide a link to
  the license, and indicate if changes were made.

To view a copy of this license, visit:
http://creativecommons.org/licenses/by/4.0/
```

---

**Official Website**: https://kreki.or.id

**GitHub Organization**: https://github.com/kreki-indonesia

**Standards Repository**: https://github.com/kreki-indonesia/ea-standards
