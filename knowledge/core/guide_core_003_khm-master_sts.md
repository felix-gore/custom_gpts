# Master Guide: Knowledge Hub Management

ID: GUIDE-KHM-MASTER-01
Version: 1.0.0
Status: Published
Human-Creator: FS
Human-Editor: FS
Model-Collaborator: IA-GEMINI
Creation-Date: 2025-07-28
Modification-Date: 2025-07-06
Primary-Source: N/A
Ref-STS-Guide: GUIDE-STS-MASTER-01

## 1. Philosophy and Core Principles

ID: GUIDE-KHM-PHILOSOPHY-01
Purp: Establish the fundamental principles for managing the Knowledge Hub as an engineering system, not as a collection of documents.
Mssn: To ensure all knowledge assets are discoverable, auditable, versionable, and reusable across a fleet of AI agents.

- Cpt: Principle 1 - Knowledge as a Managed Asset.
  - Def: Every knowledge artifact is treated with the same rigor as software code. It has a defined lifecycle, is subject to quality control, and is managed in a version control system.
- Cpt: Principle 2 - Centralized Hub, Federated Domains.
  - Def: All knowledge resides in a single, master repository (the Hub) but is strictly organized into separate, self-contained domains (`core`, `gore_nuble`, etc.). This prevents cross-contamination and simplifies governance.
- Cpt: Principle 3 - Composition over Ramification.
  - Def: Agent-specific knowledge bases are assembled by composing granular, independent artifacts.
  - Prohib: Using Git branches to manage variations of content for different agents is a critical anti-pattern. Ref: GUIDE-KHM-GIT-01.
- Cpt: Principle 4 - Explicit Governance.
  - Def: The structure, naming, and lifecycle of every knowledge asset are governed exclusively by the rules within this guide and registered in the Knowledge Catalog.
- Cpt: Principle 5 - ALM Integration.
  - Def: This guide serves as the detailed implementation of the knowledge management layer described within the Agent Lifecycle Management (ALM) framework.
  - Ref: `guide_core_002_alm-master_sts.md`.

## 2. Directory Architecture

ID: GUIDE-KHM-ARCHITECTURE-01
Purp: Define the standardized directory structure for all knowledge-related assets.
Req: This structure is mandatory for the root of the repository.

- Cpt: `/knowledge/`
  - Purp: Root directory for all validated, curated, and agent-ready knowledge artifacts.
  - Req: Only files from this directory can be referenced in an agent's `KB.GOVERNANCE.SOURCE_FILES` directive.
  - Cpt: `knowledge/core/`
    - Purp: Contains transversal, foundational knowledge.
    - Ex: Master guides for `ALM`, `ADP`, `STS`, `SFD`, and this document.
  - Cpt: `knowledge/domains/{domain_name}/`
    - Purp: Contains knowledge specific to a business area or context.
    - Ex: `gore_nuble/`, `legal_tech/`.
  - Cpt: `knowledge/catalog/`
    - Purp: Contains the master inventory of all knowledge assets.
    - Ref: GUIDE-KHM-CATALOG-01.

- Cpt: `/sources/`
  - Purp: Repository for raw, unprocessed source materials.
  - Ctx: PDFs, `.docx` files, plain text notes, images, etc.
  - Req: Files in this directory are the inputs for the curation process.

- Cpt: `/staging/`
  - Purp: A temporary, work-in-progress area for artifacts undergoing transformation.
  - Ctx: An artifact is refactored into `STS` or `SFD` format here before being published.

- Cpt: `/agents/`
  - Purp: Contains the definition files for all AI agents.
  - Ctx: Each subdirectory corresponds to a single agent and contains its `agent.yaml` file.

## 3. Asset Naming Convention

ID: GUIDE-KHM-NAMING-01
Purp: Define the strict, machine-readable convention for naming knowledge artifact files within the `/knowledge/` directory.
Mdl: `{tipo}_{dominio}_{id-num}_{descripcion-corta}_{formato}.md`

- Cpt: `tipo`. Def: Nature of the artifact.
  - `kb`: A standard knowledge base document.
  - `guide`: A meta-document that governs processes or standards.
  - `sfd`: A structured form definition artifact.
- Cpt: `dominio`. Def: Abbreviation of the domain.
  - `core`: Transversal knowledge.
  - `gn`: GORE Ñuble.
- Cpt: `id-num`. Def: 3-digit sequential identifier within its `tipo` and `dominio`.
  - Ex: `001`, `002`, `042`.
- Cpt: `descripcion-corta`. Def: 2-4 words in `kebab-case` describing the content.
  - Ex: `contexto-regional`, `guia-compras-publicas`.
- Cpt: `formato`. Def: The structural standard applied to the content.
  - `sts`: Structured Telegraphic Style.
  - `sfd`: Structured Form Definition.
- Cpt: Extension.
  - Req: The final name MUST be constructed as `_{formato}.md`.
  - Ex: `_sts.md`, `_sfd.md`.

- Ex: Correct-Filename-1. `kb_gn_001_contexto-regional_sts.md`
- Ex: Correct-Filename-2. `guide_core_001_alm-master_sts.md`
- Ex: Correct-Filename-3. `sfd_gn_005_formulario-postulacion_sfd.md`

## 4. The Knowledge Catalog

ID: GUIDE-KHM-CATALOG-01
Purp: Specify the structure, purpose, and maintenance of the master knowledge catalog.
Fnd: The catalog is the single source of truth for discovering and understanding available knowledge assets.

- Cpt: Master-File.
  - ID: `knowledge/catalog/catalog_master_sts.md`
  - Req: This file MUST exist and be maintained.
- Cpt: Entry-Structure.
  - Def: Each entry in the catalog represents one knowledge artifact and MUST provide key metadata.
  - Req: The metadata for each entry MUST include its `ID:`, `Purp:`, and `Cpt: Skeleton.`.
- Mdl: Catalog Entry Example.

  ```markdown
  ### kb_gn_001_contexto-regional_sts.md
  ID: CATALOG-GN-KB-001
  Purp: Provide the fundamental context of the Ñuble Region, including demographics, economy, and key actors.
  Cpt: Skeleton.
  - "## 1. Geographical and Demographic Data"
  - "## 2. Economic Structure"
  - "## 3. Political and Administrative Organization"
  - "## 4. Key Regional Stakeholders"
  ```

- Res: Allows for rapid assessment of an artifact's content and structure without opening the file.

## 5. Knowledge Lifecycle & Curation Process

ID: GUIDE-KHM-LIFECYCLE-01
Purp: Detail the end-to-end, auditable process for creating, validating, and publishing a knowledge artifact.
Proc: 6-Phase-Cycle.

- Cpt: Phase 1 - Sourcing.
  - Act: Identify raw source material required for an agent's knowledge base.
  - Act: Place the raw file(s) into the appropriate subdirectory within `/sources/`.
- Cpt: Phase 2 - Staging & Transformation.
  - Act: Copy the source file to a working file inside `/staging/`.
  - Act: Apply the `STS` or `SFD` refactoring methodology. Ref: `GUIDE-STS-MASTER-01`, `GUIDE-SFD-STS-MASTER-01`.
- Cpt: Phase 3 - Audit.
  - Act: Perform a compliance audit using the checklist from the relevant guide (`STS` or `SFD`).
  - Req: The artifact MUST pass 100% of the audit checks to proceed.
- Cpt: Phase 4 - Publishing.
  - Act: Determine the final, compliant filename using the official naming convention. Ref: `GUIDE-KHM-NAMING-01`.
  - Act: Move the validated file from `/staging/` to its final destination within `/knowledge/domains/{domain}/` or `/knowledge/core/`.
  - Act: Execute the KB Synchronization Protocol defined in ALM Phase 2 if the agent's platform requires it.
- Cpt: Phase 5 - Registration.
  - Act: Update the `knowledge/catalog/catalog_master_sts.md` file.
  - Act: Add a new entry for the published artifact, including its purpose and skeleton.
- Cpt: Phase 6 - Maintenance.
  - Def: An update to an existing knowledge artifact initiates a new mini-cycle.
  - Proc: The file is moved back to `staging` for modification, re-audited, and then moved back to `knowledge`, overwriting the previous version. The catalog is updated if the structure changed. The KB Synchronization Protocol MUST be re-executed to update the deployment target.

## 6. Git & Versioning Strategy

ID: GUIDE-KHM-GIT-01
Purp: Mandate the correct use of Git for version control of knowledge assets.
Fnd: The "Composition over Ramification" principle. Ref: `GUIDE-KHM-PHILOSOPHY-01`.

- Cpt: The Anti-Pattern.
  - Prohib: Creating Git branches to manage different knowledge configurations for different agents (e.g., a `feature/agent-A-kb` branch).
  - Cause: This creates an unmanageable number of merge conflicts, destroys the single source of truth for any given artifact, and makes auditing impossible.
- Cpt: The Correct Pattern: Composition at the Agent Level.
  - Instr: The knowledge base for any given agent is explicitly defined (`composed`) in its `agent.yaml` file.
  - Mech: The `KB.GOVERNANCE.SOURCE_FILES` directive lists the exact set of artifacts the agent uses.
  - Res: This approach is declarative, auditable, and maintains the integrity of each individual knowledge artifact. Git is used to version the history of each file, not to manage configuration sets.
- Mdl: Example.
  - Cpt: Agent A needs a general circular. `agents/agente_A/agent.yaml`:
    `KB.GOVERNANCE.SOURCE_FILES:: - "knowledge/gn/kb_gn_029_circular-33-general_sts.md"`
  - Cpt: Agent B needs a specific version. `agents/agente_B/agent.yaml`:
    `KB.GOVERNANCE.SOURCE_FILES:: - "knowledge/gn/kb_gn_035_circular-33-especifica_sts.md"`

- Cpt: Commit Message Convention.
  - Purp: To ensure a clear, traceable, and machine-readable history of all changes in the mono-repository.
  - Req: All commits MUST adhere to the Conventional Commits specification.
  - Ref: The full specification is detailed in `guide_core_002_alm-master_sts.md`, ID `GUIDE-ALM-GIT-COMMITS-01`.
  - Instr: For changes exclusively affecting knowledge artifacts, the `kb` type MUST be used.
  - Mdl: `type(scope): subject`
  - Ex: `kb(gn_001): update regional context with 2024 census data`
  - Ex: `feat(agent_ipr): add new workflow for form validation`
