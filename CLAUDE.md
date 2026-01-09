# KREKI CLAUDE.md

## Project Overview
KREKI (Komunitas Relawan Emergensi Kesehatan Indonesia) is a national volunteer organization providing emergency health response across Indonesia. This repository contains documentation blueprints, governance standards, and technology roadmaps for KREKI's digital ecosystem.

**Key Systems:**
- **HELP 119**: Mobile app for emergency response with volunteer geolocation
- **LMS Platform**: Digital training for Basic Life Support (BHD)
- **Governance Platform**: Organizational transparency portal

**Repository Purpose**: Documentation-only (no application code) - ensures system sustainability amid developer turnover

## Technology Stack
| Category | Technology | Notes |
|----------|-----------|-------|
| **Architecture** | Microservices (TOGAF 9.2) | Docker containerized |
| **API Gateway** | Kong / NGINX | Centralized traffic management |
| **Databases** | PostgreSQL + PostGIS | PostGIS for geospatial queries |
| **Languages** | Node.js, Go, PHP, Python | Service-dependent |
| **Healthcare** | FHIR R4 | SATUSEHAT integration |
| **Infrastructure** | Docker Swarm/K8s | Container orchestration |

## Key Directories
| Directory | Purpose | Reference |
|-----------|---------|-----------|
| `docs/ea/` | Enterprise Architecture framework | `docs/ea/index.md:1-140` |
| `docs/architecture/` | System architecture, microservices, API reference | `docs/architecture/index.md:1-67` |
| `docs/governance/` | IT governance, SLA, incident management | `docs/governance/index.md:1-70` |
| `docs/contributing/` | Development guidelines, code review | `docs/contributing/index.md:1-88` |
| `docs/about/` | Organization profile, volunteer program | `docs/about/index.md:1-79` |
| `docs/manual/` | User guides (HELP 119) | `docs/manual/help-119-guide.md:1-140` |
| `engineering/` | Technical handbook | `engineering/handbook.md:1-76` |

## Essential Commands

**Documentation repository** - no build commands. For individual services (separate repos):
```bash
git clone https://github.com/kreki/kreki-auth-service.git
npm install && npm run dev
```

**Git Workflow (Feature Branch):**
```bash
git checkout -b feat/feature-name
git commit -m "add: endpoint generate pdf certificate"
git push origin feat/feature-name
```

Reference: `docs/contributing/contribution-guide.md:22-84`

## Service Architecture
| Service | Tier | Stack | Database |
|---------|------|-------|----------|
| **Auth Service** | Tier 2 | Node.js/Go | PostgreSQL |
| **Emergency Core** | Tier 1 | Node.js/Go | PostgreSQL + PostGIS |
| **LMS Service** | Tier 3 | PHP/Python | PostgreSQL |
| **Volunteer Service** | Tier 2 | Node.js/Go | PostgreSQL + PostGIS |
| **SATUSEHAT Bridge** | Tier 2 | Node.js/Go | - |

Reference: `docs/architecture/microservices-design.md:12-23`

## Service Level Objectives (SLOs)
| Tier | Availability | Response Time | RTO |
|------|--------------|---------------|-----|
| **Tier 1** (Emergency) | 99.9% | < 500ms (P95) | 15 min |
| **Tier 2** (Auth/Volunteer) | 99.5% | < 1s (P95) | 1 hour |
| **Tier 3** (LMS/CMS) | 99% | < 2s (P95) | 4 hours |

Reference: `docs/governance/sla-slo.md:33-77`

## Contact Information
| Purpose | Contact |
|---------|---------|
| **IT Support** | it-support@kreki.or.id |
| **General** | sekretariat.kreki@gmail.com |
| **Emergency Hotline** | 08888-119-119 |

Reference: `docs/about/contact.md:8-35`

## Additional Documentation

### Enterprise Architecture
| File | When to Check |
|------|---------------|
| `.claude/docs/architectural_patterns.md` | Design decisions, microservices patterns, EA frameworks |
| `docs/ea/index.md` | EA overview with navigation |
| `docs/ea/business-architecture.md` | Business capabilities, value streams, stakeholders |
| `docs/ea/data-architecture.md` | Data domains, governance, PDP Law 2022 |
| `docs/ea/technology-architecture.md` | Technology stack, standards, technology radar |
| `docs/ea/security-architecture.md` | Security domains, Zero Trust, compliance |
| `docs/ea/integration-architecture.md` | Integration patterns, FHIR/SATUSEHAT |
| `docs/ea/innovation-framework.md` | Technology radar, emerging tech |
| `docs/ea/roadmap.md` | 3-year evolution roadmap |

### Technical & Architecture
| File | When to Check |
|------|---------------|
| `docs/architecture/api-reference.md` | API endpoints, authentication |
| `docs/architecture/microservices-design.md` | Detailed service specs, data models |
| `docs/architecture/accessibility-strategy.md` | Offline-first, multibahasa |

### Governance & Operations
| File | When to Check |
|------|---------------|
| `docs/governance/it-governance.md` | IT governance, change management, monitoring |
| `docs/governance/emergency-playbook.md` | Emergency workflows, escalation |
| `docs/governance/stakeholder-integration.md` | PSC 119 protocols, FHIR interoperability |
| `docs/governance/incident-management.md` | Incident response, severity classification |

### Organization & Development
| File | When to Check |
|------|---------------|
| `docs/about/sustainability.md` | Funding strategy, partnerships |
| `docs/about/volunteer-program.md` | BHD training, certification |
| `docs/contributing/contribution-guide.md` | Development standards, security |
| `engineering/handbook.md` | Engineering practices, ecosystem overview
