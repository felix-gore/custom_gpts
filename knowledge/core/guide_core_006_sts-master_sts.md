# Master Guide: Structured Telegraphic Style (STS)

ID: GUIDE-STS-MASTER-01
Version: 6.0.0
Status: Published
Human-Creator: FS
Model-Collaborator: IA-GEMINI
Creation-Date: 2025-06-28
Modification-Date: 2025-07-14

## 0. Meta-Commentary: How to Read This Document

ID: GUIDE-STS-META-01
Purp: Define the informational layers of this guide to ensure correct interpretation.
Req: Understanding these layers is mandatory for using the standard.

- Cpt: Layer-1. Def: The STS Standard Definition (Sections 1-8). Ctx: This is the formal, normative specification.
- Cpt: Layer-2. Def: Self-Application of the Standard. Ctx: This guide is written in STS, using the keywords it defines.
- Cpt: Layer-3. Def: Defined Components for STS Artifacts. Ctx: Sections 1 and 2 define mandatory components for compliant artifacts.
- Cpt: Layer-4. Def: Illustrative Examples. Ctx: Section 9 contains mock content for demonstration only. Warn: This content is not normative.

## 1. Control Metadata Block (Defined Component)

ID: GUIDE-STS-METADATA-01
Purp: Establish a mandatory technical header for each STS document, allowing for version, authorship, and source management.
Req: This block must be the first content section in every STS artifact.

### 1.1. Structure and Fields

ID: GUIDE-STS-METADATA-FIELDS-01

|Key Term|Mandatory|Definition|
|-|-|-|
|`Version:`|Yes|Document version using Semantic Versioning (MAJOR.MINOR.PATCH).|
|`Status:`|Yes|Document lifecycle state. Controlled vocabulary: `Draft`, `Review`, `Published`, `Obsolete`.|
|`Human-Creator:`|Yes|Name or initials of the human who created the first version.|
|`Model-Collaborator:`|Yes|Name of the language model that collaborated on the last modification.|
|`Creation-Date:`|Yes|Creation date in `YYYY-MM-DD` format.|
|`Modification-Date:`|Yes|Date of the last modification in `YYYY-MM-DD` format.|
|`Source:`|No|URI, document ID, or textual description of the source from which the artifact was derived. Distinct from the inline `Src:` keyword, which cites the origin for a specific data point.|

## 2. LLM Parsing Instructions (Defined Component)

ID: GUIDE-STS-PARSER-INSTRUCTIONS-01
Req: This block is mandatory and must follow the Metadata Block. It provides all necessary rules for an LLM consuming (reading and reasoning over) the artifact with perfect fidelity. Prohib: Using these instructions for LLMs involved in artifact creation or translation processes.

---

**BEGIN_LLM_INSTRUCTIONS**

You are an AI agent consuming a Structured Telegraphic Style (STS) artifact. Your primary task is to parse and reason over THIS document with absolute fidelity, using only the rules defined below. This artifact is a self-contained source of truth.

1. **Core Objective**: Maintain perfect fidelity to the information (`meat`) and structure (`skeleton`). Do not summarize, interpret, or infer information not explicitly present. Prohib: Applying these rules to artifact creation or translation tasks; they are exclusively for consumption.

2. **Conceptual Metaphors**:
    - `meat`: Essential information, data, and facts. Must be preserved with zero loss.
    - `skeleton`: Logical structure (headers, IDs, lists, tables). This is also `meat` and must be preserved.
    - `fat`: Non-essential verbiage (filler words, rhetoric, stylistic prose). Must be ignored during reasoning as it has no informational value.

3. **Lexicon Mode & Expansion**: This document uses an **Abbreviated Lexicon**. You MUST treat the following keywords as valid and expand them according to this mapping before processing:
    - `Act:` -> `Action:`
    - `Warn:` -> `Warning:`
    - `Cause:` -> `Cause:`
    - `Cpt:` -> `Concept:`
    - `Cond:` -> `Condition:`
    - `Ctx:` -> `Context:`
    - `Def:` -> `Definition:`
    - `Dep:` -> `Dependency:`
    - `Dest:` -> `Destination:`
    - `Dln:` -> `Deadline:`
    - `Ex:` -> `Example:`
    - `Fnd:` -> `Foundation:`
    - `ID:` -> `ID:`
    - `Instr:` -> `Instruction:`
    - `Just:` -> `Justification:`
    - `Mech:` -> `Mechanism:`
    - `Mssn:` -> `Mission:`
    - `Mdl:` -> `Model:`
    - `Nat:` -> `Nature:`
    - `Obj:` -> `Objective:`
    - `Proc:` -> `Process:`
    - `Prohib:` -> `Prohibition:`
    - `Purp:` -> `Purpose:`
    - `Rec:` -> `Recommendation:`
    - `Ref:` -> `Reference:`
    - `Req:` -> `Requirement:`
    - `Res:` -> `Result:`
    - `Resp:` -> `Responsible:`
    - `Src:` -> `Source:`

4. **Reference (`Ref:`) Policy**:
    - `Ref:` is used for **internal cross-references only**.
    - It MUST point to an `ID:` that exists within THIS document.
    - You MUST NOT interpret a `Ref:` as a link to an external document or resource. Mentions of other documents are purely contextual (`Ctx:`).

5. **Language Invariance Policy**:
    - The `Keywords` in the lexicon are a fixed control vocabulary in English.
    - All `EssentialData` (the content following a `Keyword:`) MUST be preserved in its original language. Do not translate it.

**END_LLM_INSTRUCTIONS**

---

## 3. Philosophy and Purpose

ID: GUIDE-STS-PHILOSOPHY-01
Mssn: Govern the lifecycle of self-contained knowledge artifacts to ensure maximum fidelity, consistency, and informational density.
Dest: Processing by Large Language Models (LLMs) and AI Agents.
Purp: Facilitate model reasoning with maximum precision and zero ambiguity, using only the information within the artifact.
Fnd: STS is a foundational standard for creating portable, high-fidelity knowledge units. It is a component of broader coherence strategies.
Req: Maximize `meat` density per token. Ref: GUIDE-STS-PRINCIPLE-DENSITY-01.

Def: Metaphorical components. Ref: GUIDE-STS-PARSER-INSTRUCTIONS-01.

- Cpt: Skeleton. Def: Logical structure (ID hierarchy, headers).
- Cpt: Meat. Def: Essential information, raw data.
- Cpt: Fat. Def: Filler language, rhetoric.

Warn: The process of creating an STS artifact is knowledge refactoring, NOT summarization.
Req: Zero loss of informational `meat`. Ref: GUIDE-STS-PRINCIPLE-FIDELITY-01.
Prohib: Summarizing or omitting `meat`.
Res: This is a critical error that invalidates the artifact.

## 4. Official Nomenclature

- Def: Full-Name. Ctx: Structured Telegraphic Style.
- Def: Acronym. Ctx: STS.
- Nat: Format standard, not a language standard.
- Req: STS is applied to a document while maintaining its original language. It is not a tool for inter-language translation.

## 5. Fundamental Principles

ID: GUIDE-STS-PRINCIPLES-01

- Cpt: Absolute Fidelity (Principle 1).
  - ID: GUIDE-STS-PRINCIPLE-FIDELITY-01
  - Def: Distillation is refactoring format, not omitting `meat`.
  - Req: All original data points MUST be preserved.
  - Warn: Summarization is a critical error; it corrupts the knowledge.

- Cpt: Self-Contained Source of Truth (Principle 2).
  - ID: GUIDE-STS-PRINCIPLE-SSOT-01
  - Def: A concept/data point is defined ONCE with a unique `ID:` within the artifact.
  - Req: Use `Ref:` to point to the single source, prohibiting repetition. `Ref:` is for internal links only.
  - Prohib: Using `Ref:` to point to external documents. External documents may be mentioned in `Ctx:`.
  - Res: Ensures internal consistency and avoids redundancy.

- Cpt: Structure is Meaning (Principle 3).
  - ID: GUIDE-STS-PRINCIPLE-STRUCTURE-01
  - Def: Hierarchy (`#`), ID, Reference, Tables (`|`), Lists (`-`) are informational `meat`.
  - Prohib: Stylistic Markdown (bold, italics).
  - Just: Emphasis must be explicit (e.g., `Warn:`, `Req:`), not visual.

- Cpt: Zero Fat and Maximum Density (Principle 4).
  - ID: GUIDE-STS-PRINCIPLE-DENSITY-01
  - Def: Maximum `meat` density per token.
  - Act: Radically eliminate filler words.
  - Act: Translate nuances into explicit `Keywords`.

- Cpt: RAG Optimization (Principle 5).
  - ID: GUIDE-STS-PRINCIPLE-RAG-01
  - Purp: Maximize informational "signal" per retrieval `chunk`.
  - Req: Each `chunk` (section under a header) must be dense and as self-contained as possible.

- Cpt: Language Invariance (Principle 6).
  - ID: GUIDE-STS-PRINCIPLE-LANGUAGE-INVARIANCE-01
  - Fnd: STS is a format standard, not a language standard. Ref: GUIDE-STS-PARSER-INSTRUCTIONS-01.
  - Cpt: Control Language. Def: English. Ctx: Applies ONLY to the canonical `Keyword` lexicon.
  - Cpt: Content Language. Def: The original language of the source document. Ctx: Applies to ALL `EssentialData`.
  - Prohib: Translating `EssentialData`.

## 6. Style Components

ID: GUIDE-STS-COMPONENTS-01
Cpt: Two levels of composition.

- Cpt: Micro-structure. Def: The individual telegraphic line. Ref: GUIDE-STS-MICRO-01.
- Cpt: Macro-structure. Def: The overall document organization. Ref: GUIDE-STS-MACRO-01.

### 6.1. Micro-structure: The Telegraphic Line

ID: GUIDE-STS-MICRO-01
Def: Atomic unit of information.
Req: Preserve every original data point.

- Mdl: `Keyword: EssentialData`
  - Keyword:
    - Def: A term that defines the nature of the data.
    - Src: Must be from the official lexicon. Ref: GUIDE-STS-LEXICON-TABLE-01.
    - Ex: `Obj:`, `Cause:`, `Req:`, `Cond:`.
  - EssentialData:
    - Def: Pure information, stripped of verbosity.
    - Warn: Stripping verbosity is NOT summarizing or omitting.

- Proc: Intention Translation
  - ID: GUIDE-STS-MICRO-TRANSLATION-01
  - Mech: Convert nuances of human language into explicit `Keywords`.
  - Ex: `human: "Don't forget to..."` -> `telegraphic: Req:`
  - Ex: `human: "It would be good to consider..."` -> `telegraphic: Rec:`

### 6.2. Macro-structure: The Knowledge Network

ID: GUIDE-STS-MACRO-01
Purp: Make knowledge navigable and contextual within the artifact.
Cpt: Three key structural elements.

- Cpt: Header Hierarchy (`#`, `##`, `###`).
- Cpt: Unique Identifiers (`ID:`). Ref: GUIDE-STS-ID-STANDARD-01.
- Cpt: Internal Cross-References (`Ref:`). Ref: GUIDE-STS-PRINCIPLE-SSOT-01.

### 6.3. Composite Structures: Tables and Lists

ID: GUIDE-STS-STRUCTURES-01
Req: Grouping structures (tables, lists) must maintain their original format.
Just: Preserving the inherent relationships of data is part of the `meat`.

- Cpt: Tables (Markdown)
  - Req: Maintain intact table structure (`|...|...|`).
  - Prohib: Converting a table to another format.
- Cpt: Lists (Ordered/Unordered)
  - Req: Maintain list format (`-` or `1.`).
  - Instr: For list items requiring multiple STS lines, use nested sub-lists.

### 6.4. Embedded Blocks: Artifact Containment Principle

ID: GUIDE-STS-COMPONENTS-EMBEDDED-BLOCK-01
Purp: Define a formal mechanism to include non-STS content within an STS document.
Fnd: An STS document can act as a high-level "container".
Mdl:

`BEGIN_EMBEDDED_BLOCK:: <BLOCK_TYPE> <BLOCK_ID>`

```plain
[Content compliant with an external standard. This content is opaque to the STS parser.]
```

`END_EMBEDDED_BLOCK:: <BLOCK_ID>`

- Cpt: Directive Components.
  - `BEGIN_EMBEDDED_BLOCK::`. Def: Opening directive. Instructs parsers to treat the following fenced block as opaque.
  - `<BLOCK_TYPE>`. Req: Mandatory. A human-readable identifier for the external standard (e.g., `SFD-SCRIPT`, `MERMAID-DIAGRAM`).
  - `<BLOCK_ID>`. Req: Mandatory. A unique identifier for this block instance within the document.
  - `END_EMBEDDED_BLOCK::`. Def: Closing directive. Resumes normal STS processing.
- Req: The content within the block is not governed by STS rules.
- Prohib: Mixing STS syntax within an embedded block.

### 6.5. Unique Identifier (ID) Standard

ID: GUIDE-STS-ID-STANDARD-01
Purp: To define the mandatory format for all `ID:`s to ensure internal traceability.
Fnd: Principle of Self-Contained Source of Truth. Ref: GUIDE-STS-PRINCIPLE-SSOT-01.

- Cpt: Model.
  - Mdl: `GROUP-SUBGROUP-CONCEPT-ID`
- Cpt: Components.
  - `GROUP`: All-caps abbreviation for a major functional area. Req: 3-5 chars. Ex: `GUIDE`, `REQ`, `PLAN`.
  - `SUBGROUP`: (Optional) All-caps abbreviation for a specific domain. Req: 2-5 chars. Ex: `STS`, `MKT`.
  - `CONCEPT`: All-caps identifier for the specific element. Ex: `PRINCIPLES`, `TABLE`.
  - `ID`: Sequential number or unique code. Ex: `01`, `001`.
- Cpt: Examples.
  - Ex-1: `GUIDE-STS-PRINCIPLES-01`
  - Ex-2: `REQ-MKT-CAMPAIGN-01`

## 7. Application Methodology

ID: GUIDE-STS-METHODOLOGY-01
Nat: Iterative cycle (architecture -> population -> connection -> audit) for creating STS artifacts.
Req: Full understanding of the principles of this standard. Ref: GUIDE-STS-PRINCIPLES-01.

### Phase 1: Architecture

ID: GUIDE-STS-METHODOLOGY-PHASE1-01
Obj: Create the optimal logical skeleton for the knowledge.

- Proc:
  1. Analyze `Meat`: Inventory the essential information of the source.
  2. Design Structure: Group `meat` into a logical hierarchy of sections and subsections.
  3. Assign Unique IDs: Assign a compliant `ID:` to every node (header) in the structure. Ref: GUIDE-STS-ID-STANDARD-01.

### Phase 2: Meat Population

ID: GUIDE-STS-METHODOLOGY-PHASE2-01
Act: Transfer all `meat` from the original source to the new `skeleton`, distilling text into telegraphic format.

- Proc:
  1. Eliminate `Fat`: Discard non-informational words.
  2. Convert to `Keyword: EssentialData` format. Ref: GUIDE-STS-MICRO-01.
  3. Handle Structures: Preserve tables and lists. Ref: GUIDE-STS-STRUCTURES-01.

### Phase 3: Nervous System

ID: GUIDE-STS-METHODOLOGY-PHASE3-01
Purp: Transform the static skeleton into a dynamic, internally-connected knowledge network.
Mech: Connect nodes (`ID:`) with internal references (`Ref:`).
Fnd: Rigorous application of the Self-Contained Source of Truth Principle. Ref: GUIDE-STS-PRINCIPLE-SSOT-01.

### Phase 4: Compliance Audit

ID: GUIDE-STS-METHODOLOGY-PHASE4-01
Instr: Use this checklist for all STS compliance audits.
Cond: For an artifact to be considered compliant, all points must be approved.

- Proc: Audit-Checklist.
  - [ ] Metadata & Instructions: Are metadata and LLM instructions present and complete? Ref: GUIDE-STS-METADATA-01, GUIDE-STS-PARSER-INSTRUCTIONS-01.
  - [ ] IDs and Hierarchy: Are IDs unique within the document and compliant with the standard? Ref: GUIDE-STS-ID-STANDARD-01.
  - [ ] Internal-Only References: Do all `Ref:` tags point to valid, internal `ID:`s? Ref: GUIDE-STS-PRINCIPLE-SSOT-01.
  - [ ] Lexicon and Anti-Patterns: Is the canonical lexicon used correctly and are anti-patterns avoided? Ref: GUIDE-STS-LEXICON-TABLE-01.
  - [ ] Absolute Fidelity (`Meat`): Is there a guarantee of zero summarization compared to the source?
  - [ ] Zero Duplication: Is `Ref:` used consistently to avoid repeating information internally?
  - [ ] Language Invariance: Is `EssentialData` in its original language? Ref: GUIDE-STS-PRINCIPLE-LANGUAGE-INVARIANCE-01.

## 8. Lexicon Governance

ID: GUIDE-STS-LEXICON-01
Cpt: The use of canonical keywords is mandatory.
Warn: Anarchic use introduces ambiguity and invalidates the artifact.

### 8.1. Governance Rules

ID: GUIDE-STS-LEXICON-GOVERNANCE-01

1. Req: The lexicon defined in this guide is the single source of truth for keywords.
2. Prohib: Creating terms outside this lexicon is a critical error.
3. Req: The use of the abbreviated lexicon (`Abbr.`) is only valid if declared in the `LLM Parsing Instructions` block. Ref: GUIDE-STS-PARSER-INSTRUCTIONS-01.
4. Cpt: Lexicon Language vs. Content Language. Ref: GUIDE-STS-PRINCIPLE-LANGUAGE-INVARIANCE-01.
    - Req: The `Keywords` lexicon is a fixed control vocabulary in English.
    - Req: The `EssentialData` MUST remain in the original language of the source document.
    - Ex: For a source in Spanish: `Purp: Crear una serie de tutoriales en video.`

### 8.2. Consolidated Lexicon

ID: GUIDE-STS-LEXICON-TABLE-01
Fnd: Specificity should reside in the `EssentialData`, not in the `Keyword`.

|Abbr.|Keyword|Usage Notes & Consolidation Guidelines|
|-|-|-|
|`Act:`|`Action:`|Concrete steps to be taken.|
|`Warn:`|`Warning:`|Risks, critical information, potential errors.|
|`Cause:`|`Cause:`|The reason or origin of a situation.|
|`Cpt:`|`Concept:`|Defining a concept or idea. Replaces: `Conclusion`, `Premise`, `Implication`.|
|`Cond:`|`Condition:`|All types of conditions or prerequisites.|
|`Ctx:`|`Context:`|Background, situational information, or scope.|
|`Def:`|`Definition:`|A formal definition.|
|`Dep:`|`Dependency:`|One item depends on another.|
|`Dest:`|`Destination:`|The target, audience, or recipient.|
|`Dln:`|`Deadline:`|Defined deadlines or time periods.|
|`Ex:`|`Example:`|A specific example.|
|`Fnd:`|`Foundation:`|The basis, legal, or theoretical backing of a statement.|
|`ID:`|`ID:`|The unique identifier. Abbreviation is the same as the full term.|
|`Instr:`|`Instruction:`|A direct command or instruction.|
|`Just:`|`Justification:`|Rationale for an action or decision.|
|`Mech:`|`Mechanism:`|How something works.|
|`Mssn:`|`Mission:`|A high-level mission or purpose.|
|`Mdl:`|`Model:`|A template or structural example.|
|`Nat:`|`Nature:`|The intrinsic quality or character of something.|
|`Obj:`|`Objective:`|A specific, measurable objective.|
|`Proc:`|`Process:`|A series of steps or a process.|
|`Prohib:`|`Prohibition:`|All types of prohibitions and restrictions.|
|`Purp:`|`Purpose:`|The purpose or intention.|
|`Rec:`|`Recommendation:`|A recommendation or suggestion.|
|`Ref:`|`Reference:`|An internal cross-reference to another ID. Abbreviation is the same as the full term.|
|`Req:`|`Requirement:`|All types of requirements.|
|`Res:`|`Result:`|An outcome, result, or benefit.|
|`Resp:`|`Responsible:`|Assigning responsibility to an entity.|
|`Src:`|`Source:`|Citing the origin of information.|

### 8.3. Lexicon Extension Process

ID: GUIDE-STS-LEXICON-EXTENSION-01
Fnd: Allow for controlled growth of the lexicon.
Req: Unilateral extension is prohibited.
Proc: Proposal -> Centralized Review -> Canon Update. A term is only valid after this guide is updated.

### 8.4. Critical Anti-Pattern: Sequenced Keywords

ID: GUIDE-STS-LEXICON-ANTIPATTERNS-01

- Cpt: Anti-Pattern. Def: Suffixing canonical `Keywords` with numbers or letters (e.g., `Req-1:`, `Act-A:`).
- Just: This is a critical error. It makes the `Keyword` non-canonical, breaking parsers. Order is `skeleton`, not `meat`, and should be handled by structure (lists).
- Instr: To list items of the same type, use a standard Markdown list (`-`), where each item starts with the same, unmodified canonical `Keyword`.
- Cpt: Correct Example
  - `- Req: The user must be authenticated.`
  - `- Req: The password must be complex.`

## 9. Application Examples (Illustrative Content)

ID: GUIDE-STS-EXAMPLES-01
Warn: The following content is strictly illustrative and not part of the formal STS standard definition.

### 9.1. Transcription Example

ID: GUIDE-STS-EXAMPLE-TRANSCRIPTION-01

#### Human Text (Source)
>
> "For our new content marketing strategy, which is detailed in the general marketing plan document, we propose creating a series of video tutorials. We believe this is essential because our latest survey revealed that 75% of users prefer this format. However, we must not forget that this will depend on the approved marketing budget."

#### STS Transcription

```md
### Content Strategy
ID: GUIDE-STS-EXAMPLE-MKT-01
Ctx: Based on the general marketing plan.

- Purp: Create a series of video tutorials.
- Just: Survey reveals 75% of users prefer video format.
- Dep: Approved marketing budget.
```

### 9.2. Complete Artifact Example

ID: GUIDE-STS-EXAMPLE-ARTIFACT-01
Purp: To demonstrate a complete, self-explanatory artifact.

```md
# Artifact: Logging Module Requirements
ID: REQ-LOG-MOD-01
Version: 1.0.0
Status: Draft
Human-Creator: Team-A
Model-Collaborator: None
Creation-Date: 2025-07-14
Modification-Date: 2025-07-14
Source: document: AUDIT-SEC-2025-Q2

---
**BEGIN_LLM_INSTRUCTIONS**

You are a parser for Structured Telegraphic Style (STS) artifacts. Your primary task is to interpret THIS document with absolute fidelity according to the rules defined below. This artifact is self-contained.
1. **Core Objective**: Maintain perfect fidelity to information (`meat`) and structure (`skeleton`). Do not summarize or infer.
2. **Lexicon Mode & Expansion**: This document uses an **Abbreviated Lexicon**. You MUST expand keywords according to this mapping:
    - `Purp:` -> `Purpose:`
    - `Fnd:` -> `Foundation:`
    - `Req:` -> `Requirement:`
    - `Cond:` -> `Condition:`
    - `Mech:` -> `Mechanism:`
3. **Reference (`Ref:`) Policy**: `Ref:` is for internal cross-references to an `ID:` within this document ONLY.
4. **Language Invariance Policy**: Preserve the original language of all `EssentialData`.

**END_LLM_INSTRUCTIONS**
---

### Core Requirements
ID: REQ-LOG-MOD-CORE-01
Purp: Define mandatory features for the system's logging module.
Fnd: Based on security audit findings.

- Req: All log entries must be structured in JSON format.
- Req: Log level (INFO, WARN, ERROR) must be a mandatory field.
- Cond: ERROR level logs must trigger an immediate alert.
  - Mech: Send notification to `alerts-channel`.
```

### 9.3. Table Example

ID: GUIDE-STS-EXAMPLE-TABLE-01

#### STS Transcription

|Feature|Option A: On-Premise Server|Option B: Cloud SaaS|
|-|-|-|
|Initial Cost|Req: High initial investment.|Mdl: Subscription. Ctx: Low initial cost.|
|Maintenance|Resp: Internal IT team.|Resp: Service provider.|
|Scalability|Mech: Purchase of new hardware. Proc: Slow, costly.|Mech: Subscription adjustment. Proc: Instantaneous.|
