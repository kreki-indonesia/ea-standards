# Architectural Patterns

## Documentation Structure Patterns

### Markdown Frontmatter Pattern
**Description**: All documentation files use YAML frontmatter with standardized metadata fields
**Locations**: `docs/business-architecture.md:1-6`, `docs/data-architecture.md:1-6`, `docs/technology-architecture.md:1-6`
**Rationale**: Provides consistent metadata for documentation indexing, searchability, and last update tracking

**Pattern Template**:
```yaml
---
title: "Document Title"
description: "Brief description"
category: "category-name"
last_updated: YYYY-MM-DD
---
```

### TOGAF 9.2 Domain Organization
**Description**: Enterprise Architecture documentation follows TOGAF 9.2 ADM phases with four core domains
**Locations**: `docs/business-architecture.md`, `docs/data-architecture.md`, `docs/application-architecture.md`, `docs/technology-architecture.md`
**Rationale**: Industry-standard framework for emergency services EA ensures comprehensive coverage and stakeholder alignment

**Domain Structure**:
- **Business Architecture** (`docs/business-architecture.md`): Capabilities, value streams, organizational structure
- **Data Architecture** (`docs/data-architecture.md`): Data domains, FHIR integration, PostGIS geospatial
- **Application Architecture** (`docs/application-architecture.md`): Microservices portfolio, lifecycle management
- **Technology Architecture** (`docs/technology-architecture.md`): Stack standards, infrastructure patterns
- **Security Architecture** (`docs/security-architecture.md`): Zero Trust, PDP Law 2022 compliance
- **Integration Architecture** (`docs/integration-architecture.md`): FHIR R4, SATUSEHAT, API patterns

### Three-Tier Licensing Model
**Description**: Organization repositories categorized by licensing level for appropriate IP protection
**Locations**: `.claude/DEVELOPMENT_NOTES.md:13-16`, `LICENSE`, `README.md`
**Rationale**: Balances open standards adoption with commercial platform viability

**Categories**:
- **Layer 1 (Standards)**: CC BY 4.0, MIT, Apache 2.0 - Open source reference standards
- **Layer 2 (Platform)**: KSAL (KREKI Source Available License) - Source visible, licensed deployment
- **Layer 3 (Org-specific)**: Proprietary - KREKI-only assets, private repositories

### Indonesian-English Bilingual Documentation
**Description**: Documentation supports both Indonesian (Bahasa Indonesia) and English
**Locations**: `docs/index.md` (Indonesian), `docs/README.md` (English)
**Rationale**: Serves Indonesian national emergency services while enabling international collaboration

## Microservices Patterns

### Service Tier Classification
**Description**: Services categorized by criticality with scaling and HA requirements
**Locations**: `docs/microservices-design.md:14-22`
**Rationale**: Aligns infrastructure investment with mission-critical needs (survival outcomes)

**Tiers**:
- **Tier 1 (Critical)**: Emergency Core, requires HA, 2+ instances
- **Tier 2 (Important)**: Auth, Volunteer, SATUSEHAT Bridge, 2+ instances
- **Tier 3 (Supporting)**: LMS, Notification, Content, 1+ instance

### RESTful API Design Conventions
**Description**: All microservices follow consistent REST API patterns with OpenAPI 3.0 specification
**Locations**: `docs/api-reference.md`, `docs/microservices-design.md:30-40` (Auth endpoints), `docs/microservices-design.md:85-93` (Emergency endpoints)
**Rationale**: Standardized interface enables interoperability and client SDK generation

**API Patterns**:
- POST for creation (registration, panic button trigger)
- GET for retrieval (user profile, active emergencies)
- PUT for updates (respond to emergency, complete emergency)
- Resource naming: `/api/{service}/{resource}/{id}`

### Geospatial Query Pattern (PostGIS)
**Description**: Volunteer matching uses PostGIS ST_Distance within radius queries
**Locations**: `docs/microservices-design.md:96-110`
**Rationale**: Enables efficient location-based volunteer discovery for emergency response

**SQL Pattern**:
```sql
SELECT v.id, v.full_name, v.location
FROM volunteers v
WHERE v.status = 'available'
  AND v.skills @> '{skills}'
  AND ST_DWithin(v.location, ST_MakePoint(lng, lat), radius)
ORDER BY ST_Distance(v.location, ST_MakePoint(lng, lat))
LIMIT 20;
```

## Healthcare Integration Patterns

### FHIR R4 Resource Mapping
**Description**: Healthcare data exchange follows HL7 FHIR R4 resources for Indonesian interoperability
**Locations**: `docs/integration-architecture.md`, `docs/data-architecture.md`
**Rationale**: National standard (SATUSEHAT) compliance and healthcare system integration

**Key Resources**:
- **Patient**: Demographics and medical history
- **Observation**: Vital signs and assessments
- **Location**: Emergency incident location
- **Practitioner**: Volunteer and healthcare worker profiles

### SATUSEHAT Bridge Pattern
**Description**: Integration with Indonesia's national health data platform through dedicated bridge service
**Locations**: `docs/integration-architecture.md`, `docs/microservices-design.md` (SATUSEHAT Bridge service)
**Rationale**: Single point of integration for national platform compliance and data aggregation

**Integration Flow**:
1. Emergency Core generates FHIR resources
2. SATUSEHAT Bridge authenticates with Kemenkes API
3. Bridge transforms and routes to SATUSEHAT endpoints
4. Response data mapped back to internal models

## Data Governance Patterns

### PDP Law 2022 Compliance
**Description**: All data handling complies with Indonesian Personal Data Protection Law
**Locations**: `docs/security-architecture.md`, `docs/data-architecture.md:privacy-section`
**Rationale**: Legal requirement for Indonesian healthcare data processing

**Compliance Patterns**:
- Explicit consent for data collection
- Data minimization principles
- Right to data portability (GPDR-aligned)
- Data breach notification requirements

### Zero Trust Security Architecture
**Description**: Security follows Never Trust, Always Verify principles
**Locations**: `docs/security-architecture.md`, `docs/incident-management.md`
**Rationale**: Healthcare emergency data requires highest security posture

**Security Layers**:
- Identity verification at every request
- Least privilege access control
- Microsegmentation between services
- Continuous monitoring and audit logging

## Contribution Workflow

### RFC (Request for Comments) Process
**Description**: Standards changes require formal RFC process with Technical Committee approval
**Locations**: `docs/ea-governance.md`, `CONTRIBUTING.md`
**Rationale**: Ensures EA standards remain stable and consensus-driven

**RFC Flow**:
1. Proposal submitted via GitHub Issue
2. Technical Committee review (monthly)
3. Public comment period (3 weeks)
4. Technical Board vote (2/3 majority)
5. Publication and version update

### Conventional Commits
**Description**: Git commit messages follow Angular convention for changelog generation
**Locations**: `CONTRIBUTING.md:commit-section`
**Rationale**: Automated changelog generation and semantic versioning

**Commit Format**: `type(scope): description`

**Types**:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `chore`: Maintenance tasks
- `refactor`: Code restructuring
- `test`: Test additions
