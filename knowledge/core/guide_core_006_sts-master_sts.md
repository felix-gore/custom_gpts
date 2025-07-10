# Master Guide: Structured Telegraphic Style (STS)

ID: GUIDE-STS-MASTER-01
Version: 5.0.0
Status: Published
Human-Creator: FS
Human-Editor: FS
Model-Collaborator: IA-GEMINI
Creation-Date: 2025-06-28
Modification-Date: 2025-07-10
Primary-Source: N/A
Ref-STS-Guide: GUIDE-STS-MASTER-01

## 1. Control Metadata Block

ID: GUIDE-STS-METADATA-01
Purp: Establish a mandatory technical header for each STS document, allowing for version, authorship, and source management.
Req: This block must be the first content section in every STS artifact.

### 1.1. Structure and Fields

ID: GUIDE-STS-METADATA-FIELDS-01

|Key Term|Mandatory|Definition (`Def:`)|
|-|-|-|
|`Version:`|Yes|Document version using Semantic Versioning (MAJOR.MINOR.PATCH).|
|`Status:`|Yes|Document lifecycle state. Controlled vocabulary: `Draft`, `Review`, `Published`, `Obsolete`.|
|`Human-Creator:`|Yes|Name or initials of the human who created the first version.|
|`Human-Editor:`|Yes|Name or initials of the human who directed the last modification.|
|`Model-Collaborator:`|Yes|Name of the language model that collaborated on the last modification.|
|`Creation-Date:`|Yes|Creation date in `YYYY-MM-DD` format.|
|`Modification-Date:`|Yes|Date of the last modification in `YYYY-MM-DD` format.|
|`Primary-Source:`|Conditional|Original document from which it was transcribed. Req: Mandatory if it is a transcription.|
|`Ref-STS-Guide:`|Yes|The `ID:` of the STS Master Guide version used for transcription or audit.|

## 2. Philosophy and Purpose

ID: GUIDE-STS-PHILOSOPHY-01
Mssn: Govern the complete lifecycle (creation, structured transcription, and audit) of STS knowledge artifacts to ensure maximum fidelity, consistency, and informational density, regardless of the original language.
Dest: Processing by Large Language Models (GPTs).
Purp: Facilitate model reasoning with maximum precision, minimum ambiguity.
Fnd: STS is a foundational component of the ALM Coherence Stack. Ref: `guide_core_002_alm-master_sts.md`.
Req: Maximize `meat` density per token. Ref: GUIDE-STS-PRINCIPLE-DENSITY-01.

Def: Metaphorical components.

- Cpt: Skeleton. Def: Logical structure (ID hierarchy, headers).
- Cpt: Meat. Def: Essential information, raw data, in its original language.
- Cpt: Fat. Def: Filler language, connectors, rhetoric, stylistic Markdown.

Warn: Process is NOT summarization. It is knowledge refactoring. Distilling `fat` cannot result in loss of `meat`.
Req: Zero loss of informational `meat`. Ref: GUIDE-STS-PRINCIPLE-FIDELITY-01.
Prohib: Summarizing or omitting informational `meat`.
Res: Critical error. Invalidates the knowledge base.

## 3. Official Nomenclature

ID: GUIDE-STS-NOMENCLATURE-01

- Def: Full-Name. Ctx: Structured Telegraphic Style.
- Def: Acronym. Ctx: STS.
- Nat: Format standard, not a language standard.
- Req: STS is applied to a document while maintaining its original language. It is not a tool for inter-language translation.

## 4. Fundamental Principles

ID: GUIDE-STS-PRINCIPLES-01

- Cpt: Principle-1: Absolute Fidelity.
  - ID: GUIDE-STS-PRINCIPLE-FIDELITY-01
  - Def: Distillation is refactoring format, not omitting `meat`.
  - Req: All original data points MUST be preserved.
  - Warn: Summarization is a critical error; it corrupts the KB.

- Cpt: Principle-2: Single Source of Truth (SSoT).
  - ID: GUIDE-STS-PRINCIPLE-DUPLICATION-01
  - Def: A concept/data point is defined ONCE with a unique `ID:`.
  - Req: Use `Ref:` to point to the single source, prohibiting repetition.
  - Res: Ensures consistency, avoids redundancy.

- Cpt: Principle-3: Structure is Meaning.
  - ID: GUIDE-STS-PRINCIPLE-STRUCTURE-01
  - Def: Hierarchy (`#`), ID, Ref, Tables (`|`), Lists (`-`) are informational `meat`.
  - Prohib: Stylistic Markdown (bold, italics).
  - Just: Emphasis must be explicit (e.g., `Warn:`, `Req:`), not visual.

- Cpt: Principle-4: Zero Fat and Maximum Density.
  - ID: GUIDE-STS-PRINCIPLE-DENSITY-01
  - Def: Maximum `meat` density per token.
  - Act: Radically eliminate filler words.
  - Act: Translate nuances into explicit `Key Terms`.

- Cpt: Principle-5: RAG Optimization.
  - ID: GUIDE-STS-PRINCIPLE-RAG-01
  - Purp: Maximize informational "signal" per retrieval `chunk`.
  - Req: Each `chunk` (section under a header) must be dense and self-contained.

- Cpt: Principle-6: Language Invariance.
  - ID: GUIDE-STS-PRINCIPLE-TRANSLATION-01
  - Fnd: STS is a format standard, not a language standard.
  - Cpt: Control Language. Def: English. Ctx: Applies ONLY to the canonical `KeyTerm` lexicon.
  - Cpt: Content Language. Def: The original language of the source document. Ctx: Applies to ALL `EssentialData`.
  - Prohib: Translating `EssentialData`.
  - Warn: Critical error equivalent to summarization.

## 5. Style Components

ID: GUIDE-STS-COMPONENTS-01
Cpt: Two levels of composition.

- Ref: GUIDE-STS-MICRO-01. Ctx: Micro-structure (individual line).
- Ref: GUIDE-STS-MACRO-01. Ctx: Macro-structure (document organization).

### 5.1. Micro-structure: The Telegraphic Line

ID: GUIDE-STS-MICRO-01
Def: Atomic unit of information.
Req: Preserve every original data point.

- Mdl: `KeyTerm: EssentialData`
  - KeyTerm:
    - Def: Word (or compound) that defines the nature of the data.
    - Src: Must be an official abbreviation from the lexicon. Ref: GUIDE-STS-LEXICON-TABLE-01.
    - Ex: `Obj:`, `Cause:`, `Req:`, `Cond:`.
  - EssentialData:
    - Def: Pure information, stripped of verbosity.
    - Warn: Stripping verbosity is NOT summarizing or omitting.
    - Req: If the original data is a list of 5 items, all 5 items must be present.

- Proc: Intention Translation
  - ID: GUIDE-STS-MICRO-TRANSLATION-01
  - Mech: Convert nuances of human language into explicit `Key Terms`.
  - Ex: `human: "Don't forget to..."` -> `telegraphic: Req:`
  - Ex: `human: "It would be good to consider..."` -> `telegraphic: Rec:`
  - Ex: `human: "This happens because..."` -> `telegraphic: Cause:`

### 5.2. Macro-structure: The Knowledge Network

ID: GUIDE-STS-MACRO-01
Purp: Make knowledge navigable and contextual.
Cpt: Three key structural elements.

- Cpt: Header Hierarchy (`#`, `##`, `###`).
- Cpt: Unique Identifiers (`ID:`). Ref: GUIDE-STS-ID-STANDARD-01.
- Cpt: Cross-References (`Ref:`).

### 5.3. Composite Structures: Tables and Lists

ID: GUIDE-STS-STRUCTURES-01
Req: Grouping structures (tables, lists) must maintain their original format.
Just: Preserving the inherent relationships of data is part of the `meat`.

- Cpt: Tables (Markdown)
  - Req: Maintain intact table structure (`|...|...|`).
  - Prohib: Converting a table to another format.
  - Act: Translate the content of EACH CELL into STS format.
  - Warn: Breaking the table is a loss of information.

- Cpt: Lists (Ordered/Unordered)
  - Req: Maintain list format (`-` or `1.`).
  - Act: Translate each item into one or more STS lines.
  - Instr: See list handling techniques. Ref: GUIDE-STS-METHODOLOGY-PHASE2-STRUCTURES-01.

### 5.4. Embedded Blocks: Artifact Containment Principle

ID: GUIDE-STS-COMPONENTS-EMBEDDED-BLOCK-01
Purp: Define a formal mechanism to include artifacts governed by other standards within an STS document, without compromising the integrity of any standard.
Fnd: Artifact Containment Principle. An STS document can act as a high-level "container".
Mdl:

- Cpt: Block Syntax.
  - `BEGIN_EMBEDDED_BLOCK:: <BLOCK_TYPE> <BLOCK_ID>`
  - `... embedded artifact content ...`
  - `END_EMBEDDED_BLOCK:: <BLOCK_ID>`
- Cpt: Directive Components.
  - `BEGIN_EMBEDDED_BLOCK::`. Def: Opening directive. Instructs parsers to halt STS processing and switch to a new parsing context.
  - `<BLOCK_TYPE>`. Req: Mandatory. The `ID:` of the guide document that governs the block's content (e.g., `GUIDE-SFD-STS-MASTER-01`).
  - `<BLOCK_ID>`. Req: Mandatory. A unique identifier for this block instance.
  - `END_EMBEDDED_BLOCK::`. Def: Closing directive. Resumes normal STS processing.
- Req: The content within the block must be 100% compliant with the standard defined in `<BLOCK_TYPE>`.
- Prohib: Mixing STS syntax within an embedded block.

## 6. Application Methodology

ID: GUIDE-STS-METHODOLOGY-01
Nat: Iterative cycle (architecture -> population -> connection -> audit) for the creation and validation of STS artifacts.
Req: Full understanding of the principles and components of this standard. Ref: GUIDE-STS-PRINCIPLES-01.

### Phase 1: Architecture

ID: GUIDE-STS-METHODOLOGY-PHASE1-01
Obj: Create the optimal logical skeleton for the knowledge.

- Proc:
  1. Original `Meat` Analysis:
      - Act: Inventory the `meat` of the source text.
  2. Trunk Design (Central Idea):
      - Act: Define the fundamental `Purp:` of the artifact.
  3. Main Branches Design (Macro-themes):
      - Act: Group `meat` into 3-7 thematic/functional areas.
      - Req: Themes must be mutually exclusive, collectively exhaustive.
  4. Secondary Branches and Leaves Design (Micro-themes):
      - Act: Break down each main branch into sub-themes and data.
  5. Assign Unique IDs:
      - Act: Assign a unique and descriptive `ID:` to EVERY NODE in the tree.
      - Req: ID must be unique across the entire knowledge base. Ref: GUIDE-STS-ID-STANDARD-01.

### Phase 2: Meat

ID: GUIDE-STS-METHODOLOGY-PHASE2-01
Req: Well-defined skeleton from Phase 1.
Act: Transfer all `meat` from the original doc to the new `skeleton`. Distill text into telegraphic format.

- Proc:
  1. Eliminate Linguistic Fat:
      - Act: Discard words with no informational value (connectors, rhetoric, etc.).
  2. Convert to `KeyTerm: EssentialData` format:
      - Act: Identify the core idea of the sentence and choose the `Key Term` from the lexicon.
  3. Handling Composite Structures:
      - ID: GUIDE-STS-METHODOLOGY-PHASE2-STRUCTURES-01
      - Req: Preserve original format (table/list). Translate content to STS. Ref: GUIDE-STS-STRUCTURES-01.
      - Instr: For list items requiring multiple STS lines, use nested sub-lists.
      - Warn: Creating numbered or sequenced KeyTerms is a critical anti-pattern. Ref: GUIDE-STS-LEXICON-ANTIPATTERNS-01.

### Phase 3: Nervous System

ID: GUIDE-STS-METHODOLOGY-PHASE3-01
Purp: Transform static skeleton -> dynamic knowledge network.
Mech: Connect nodes (`ID`) with references (`Ref`).
Fnd: Rigorous application of the Single Source of Truth Principle. Ref: GUIDE-STS-PRINCIPLE-DUPLICATION-01.

- Proc:
  1. Verify uniqueness of all IDs.
  2. Add Cross-References (`Ref:`) to eliminate `meat` duplication.

### Phase 4: Compliance Audit

ID: GUIDE-STS-METHODOLOGY-PHASE4-01
Instr: Use this checklist for all STS standard compliance audits. It is a cyclical quality control, not a final step.
Cond: For an artifact to be considered compliant, all points must be approved.

Proc: Audit-Checklist.

- [ ] Metadata Block: Is it present and complete? Ref: GUIDE-STS-METADATA-01.
- [ ] IDs and Hierarchy: Are IDs unique and compliant with the standard? Ref: GUIDE-STS-ID-STANDARD-01.
- [ ] Lexicon and Anti-Patterns: Is the canonical lexicon used and are anti-patterns avoided? Ref: GUIDE-STS-LEXICON-CONSOLIDATION-01.
- [ ] Absolute Fidelity (`Meat`): Is there a guarantee of zero summarization or omission compared to the source?
- [ ] Zero Duplication (`Ref:`): Is `Ref:` used consistently to avoid repeating information?
- [ ] Zero Fat: Has all linguistic and formatting fat (e.g., `...`) been eliminated?
- [ ] Language Invariance (Content): Is all `EssentialData` in the original source language, without translation? Ref: GUIDE-STS-PRINCIPLE-TRANSLATION-01.

## 7. Lexicon Governance

ID: GUIDE-STS-LEXICON-01
Cpt: The use of canonical abbreviations is key but requires strict governance.
Warn: Anarchic use introduces ambiguity and destroys the knowledge base.

### 7.1. Governance Rules

ID: GUIDE-STS-LEXICON-GOVERNANCE-01

1. Req: This section is the single source of truth for abbreviations.
2. Prohib: Creating terms outside this lexicon is a critical error.
3. Req: The use of the lexicon defined here is mandatory.
4. Cpt: Lexicon Language vs. Content Language.
    - Fnd: The principle of Language Invariance is absolute. Ref: GUIDE-STS-PRINCIPLE-TRANSLATION-01.
    - Req: The `Key Terms` lexicon is a fixed control vocabulary based on English.
    - Req: The `EssentialData` MUST remain in the original language of the source document.
    - Ex: For a text in Spanish, the line would be `Purp: Crear una serie de tutoriales en video.`.

### 7.2. Consolidated Lexicon

ID: GUIDE-STS-LEXICON-TABLE-01
Fnd: Specificity should reside in the `EssentialData`, not in the `KeyTerm`.

|Abbreviation|Full Term|Usage Notes & Consolidation Guidelines|
|-|-|-|
|`Act:`|Action|Use for: Concrete steps or actions to be taken.|
|`Warn:`|Warning|Use for: Highlighting risks, critical information, or potential errors.|
|`Cause:`|Cause|Use for: Explaining the reason or origin of a situation.|
|`Cpt:`|Concept|Use for: Defining a concept or idea. Replaces: `Conclusion`, `Premise`, `Implication`, `Classification`, `Types`, `Scope`.|
|`Cond:`|Condition|Use for: All types of conditions or prerequisites. Replaces: `Legal-Cond`.|
|`Ctx:`|Context|Use for: Providing background, situational information, or scope. Replaces: `Note`, `Version`, `Update-Date`.|
|`Def:`|Definition|Use for: Providing a formal definition.|
|`Dep:`|Dependency|Use for: Indicating that one item depends on another.|
|`Dest:`|Destination|Use for: Specifying the target, audience, or recipient.|
|`Dln:`|Deadline|Use for: Defined deadlines or time periods.|
|`Ex:`|Example|Use for: Providing a specific example.|
|`Fnd:`|Foundation|Use for: The basis, legal, or theoretical backing of a statement. Replaces: `Reg-Framework`, `Norm-Basis`, `Legal-Ref`.|
|`ID:`|Identifier|Standard. Do not modify.|
|`Instr:`|Instruction|Use for: Giving a direct command or instruction.|
|`Just:`|Justification|Use for: Providing the rationale or justification for an action or decision.|
|`Mech:`|Mechanism|Use for: Describing how something works. Replaces: `Operationalization`, `Methodology`, `Platform`.|
|`Mssn:`|Mission|Use for: Stating a high-level mission or purpose.|
|`Mdl:`|Model|Use for: Describing a model, template, or structural example.|
|`Nat:`|Nature|Use for: Describing the intrinsic quality or character of something.|
|`Obj:`|Objective|Use for: Stating a specific, measurable objective. Replaces: `Doc-Goal`, `Aim`.|
|`Proc:`|Process|Use for: Describing a series of steps or a process. Replaces: `Bi-phasic-Process`, `Op-Instrument`.|
|`Prohib:`|Prohibition|Use for: All types of prohibitions and restrictions. Replaces: `Key-Restriction`, `Limitations`.|
|`Purp:`|Purpose|Use for: Stating the purpose or intention. Replaces: `Exclusive-Purpose`.|
|`Rec:`|Recommendation|Use for: Providing a recommendation or suggestion.|
|`Ref:`|Reference|Standard. Do not modify.|
|`Req:`|Requirement|Use for: All types of requirements. Replaces: `Pre-Req`, `General-Req`, `Critical-Req`, `Mandate`, `Compliance`.|
|`Res:`|Result|Use for: Describing an outcome, result, or benefit. Replaces: `Expected-Outcome`, `Benefits`, `Product`.|
|`Resp:`|Responsible|Use for: Assigning responsibility to an actor, role, or entity. Replaces: `GORE-Function`, `Gov-Attribute`, `Eval-Body`.|
|`Src:`|Source|Use for: Citing the origin of information or a document. Replaces: `Primary-Legal-Basis`, `Key-Regulation`.|

### 7.3. Lexicon Extension Process

ID: GUIDE-STS-LEXICON-EXTENSION-01
Fnd: Allow for controlled growth of the lexicon without compromising consistency.
Req: Unilateral extension is prohibited. Any addition must follow this process.

- Proc:
  1. Needs Validation: Demonstrate that the current lexicon is insufficient.
  2. Formal Proposal: Submit a request (term, def, just, ex) to the standard's custodian.
  3. Centralized Review and Approval: The custodian evaluates the proposal.
  4. Canon Update: If approved, the custodian updates this guide. The term is only valid after the update.

### 7.4. Critical Anti-Pattern: Sequenced KeyTerms

ID: GUIDE-STS-LEXICON-ANTIPATTERNS-01

- Cpt: Anti-Pattern. Def: Suffixing canonical `KeyTerms` with numbers or letters (e.g., `Req-1:`, `Act-A:`, `Cond-2:`).
- Just: This practice is a critical error. It makes the `KeyTerm` non-canonical, breaking parsers and searches. It conflates the *identity* of the information (the `KeyTerm`) with its *order* in a list, which should be handled by structure (lists), not by modifying the term itself. The order is structural `meat`, not lexical `meat`.
- Instr: To express a list of items of the same type, use a standard Markdown list (`-`), where each list item begins with the same, unmodified canonical `KeyTerm`.
- Cpt: Incorrect Example
  - `Req-1: The user must be authenticated.`
  - `Req-2: The password must be complex.`
- Cpt: Correct Example
  - `- Req: The user must be authenticated.`
  - `- Req: The password must be complex.`

## 8. Application Examples

ID: GUIDE-STS-EXAMPLES-01

### 8.1. Transcription Example (English to STS)

ID: GUIDE-STS-EXAMPLE-EN-01

#### Human Text (English)
>
> "For our new content marketing strategy, which is detailed in the marketing plan, we propose creating a series of video tutorials. We believe this is essential because our latest survey revealed that 75% of users prefer this format. However, we must not forget that this will depend on the approved marketing budget, which is described in the financial document."

#### STS Transcription

```md
### Content Strategy

ID: EX-MKT-CONTENTS-01
Ctx: Marketing Plan. Ref: PLAN-MKT-GENERAL-01

- Purp: Create a series of video tutorials.
- Just: Survey reveals 75% of users prefer video format.
- Dep: Budget approval. Ref: FIN-BUDGET-MKT-01.
```

### 8.2. Table Example

ID: GUIDE-STS-EXAMPLE-TABLE-01

#### Human Table (Detailed Example)

|Feature|Option A: On-Premise Server|Option B: Cloud SaaS|
|-|-|-|
|Initial Cost|Requires a very significant initial investment because all hardware and software licenses must be purchased upfront.|Generally, the initial cost is much lower, as it operates on a monthly or annual subscription model.|
|Maintenance|Responsibility for maintenance falls entirely on the company's internal IT team, including updates and security patches.|The service provider handles all maintenance, freeing the internal team from this workload.|
|Scalability|To scale, more hardware must be purchased, which can be a slow and quite costly process.|Scalability is almost instantaneous; usually, you just need to adjust the subscription plan to get more resources.|

#### STS Transcription

|Feature|Option A: On-Premise Server|Option B: Cloud SaaS|
|-|-|-|
|Initial Cost|Req: High initial investment (hardware, license purchase).|Mdl: Subscription (monthly/annual). Ctx: Low initial cost.|
|Maintenance|Resp: Internal IT team (incl. updates, patches).|Resp: Service provider.|
|Scalability|Mech: Purchase of additional hardware. Proc: Slow, costly.|Mech: Subscription plan adjustment. Proc: Instantaneous.|

### 8.3. Example Analysis

ID: GUIDE-STS-ANALYSIS-EXAMPLES-01
Res:

- Cpt: Efficiency. Def: Significant token reduction.
- Cpt: Clarity. Def: Use of explicit `Key Terms` eliminates ambiguity.
- Cpt: Fidelity. Def: All original `meat` is preserved.
