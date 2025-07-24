# Master Guide: Structured Telegraphic Style (STS)

ID: GUIDE-STS-MASTER-01
Version: 5.2.0
Status: Published
Human-Creator: FS
Model-Collaborator: IA-GEMINI
Creation-Date: 2025-06-28
Modification-Date: 2025-07-12

## 1. Control Metadata Block

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

## 2. STS Runtime Directives Block

ID: GUIDE-STS-DIRECTIVES-01
Purp: To declare the operational mode of the STS artifact, ensuring the parsing LLM has the necessary context for a correct interpretation.
Req: This block is mandatory and must immediately follow the Control Metadata Block.
Warn: The absence of this block constitutes a non-compliant artifact.

### 2.1. Structure and Directives

- Concept: Directive.
  - Def: A single line that sets a mandatory rule for the artifact's interpretation.
  - Model: `STS-Directive: <Directive-Name> = <Value>`
- Concept: Mandatory Directives.
  - `STS-Directive: Lexicon-Mode = <Mode>`
    - Def: Instructs the parser on which keyword set to use.
    - Ctx: Supported `<Mode>` values are `Full` or `Abbreviated`. If `Abbreviated`, the parser MUST use the official `Abbr.` from the lexicon table. Ref: GUIDE-STS-LEXICON-TABLE-01.
  - `STS-Directive: STS-Version-Compliance = <Version>`
    - Def: Declares the specific version of the STS guide (e.g., `5.2.0`) the artifact complies with.
    - Ctx: Guarantees parsing fidelity according to the specified version's rules and prevents backwards-compatibility issues.

## 3. Philosophy and Purpose

ID: GUIDE-STS-PHILOSOPHY-01
Mission: Govern the complete lifecycle (creation, structured transcription, and audit) of STS knowledge artifacts to ensure maximum fidelity, consistency, and informational density, regardless of the original language.
Destination: Processing by Large Language Models (GPTs).
Purpose: Facilitate model reasoning with maximum precision, minimum ambiguity.
Foundation: STS is a foundational component of the ALM Coherence Stack. Reference: `guide_core_002_alm-master_sts.md`.
Requirement: Maximize `meat` density per token. Reference: GUIDE-STS-PRINCIPLE-DENSITY-01.

Definition: Metaphorical components.

- Concept: Skeleton. Definition: Logical structure (ID hierarchy, headers).
- Concept: Meat. Definition: Essential information, raw data, in its original language.
- Concept: Fat. Definition: Filler language, connectors, rhetoric, stylistic Markdown.

Warning: Process is NOT summarization. It is knowledge refactoring. Distilling `fat` cannot result in loss of `meat`.
Requirement: Zero loss of informational `meat`. Reference: GUIDE-STS-PRINCIPLE-FIDELITY-01.
Prohibition: Summarizing or omitting informational `meat`.
Result: Critical error. Invalidates the knowledge base.

## 4. Official Nomenclature

- Definition: Full-Name. Context: Structured Telegraphic Style.
- Definition: Acronym. Context: STS.
- Nature: Format standard, not a language standard.
- Requirement: STS is applied to a document while maintaining its original language. It is not a tool for inter-language translation.

## 5. Fundamental Principles

ID: GUIDE-STS-PRINCIPLES-01

- Concept: Principle-1: Absolute Fidelity.
  - ID: GUIDE-STS-PRINCIPLE-FIDELITY-01
  - Definition: Distillation is refactoring format, not omitting `meat`.
  - Requirement: All original data points MUST be preserved.
  - Warning: Summarization is a critical error; it corrupts the KB.

- Concept: Principle-2: Single Source of Truth (SSoT).
  - ID: GUIDE-STS-PRINCIPLE-DUPLICATION-01
  - Definition: A concept/data point is defined ONCE with a unique `ID:`.
  - Requirement: Use `Reference:` to point to the single source, prohibiting repetition.
  - Result: Ensures consistency, avoids redundancy.

- Concept: Principle-3: Structure is Meaning.
  - ID: GUIDE-STS-PRINCIPLE-STRUCTURE-01
  - Definition: Hierarchy (`#`), ID, Reference, Tables (`|`), Lists (`-`) are informational `meat`.
  - Prohibition: Stylistic Markdown (bold, italics).
  - Justification: Emphasis must be explicit (e.g., `Warning:`, `Requirement:`), not visual.

- Concept: Principle-4: Zero Fat and Maximum Density.
  - ID: GUIDE-STS-PRINCIPLE-DENSITY-01
  - Definition: Maximum `meat` density per token.
  - Action: Radically eliminate filler words.
  - Action: Translate nuances into explicit `Keywords`.

- Concept: Principle-5: RAG Optimization.
  - ID: GUIDE-STS-PRINCIPLE-RAG-01
  - Purpose: Maximize informational "signal" per retrieval `chunk`.
  - Requirement: Each `chunk` (section under a header) must be dense and self-contained.

- Concept: Principle-6: Language Invariance.
  - ID: GUIDE-STS-PRINCIPLE-TRANSLATION-01
  - Foundation: STS is a format standard, not a language standard.
  - Concept: Control Language. Definition: English. Context: Applies ONLY to the canonical `Keyword` lexicon.
  - Concept: Content Language. Definition: The original language of the source document. Context: Applies to ALL `EssentialData`.
  - Prohibition: Translating `EssentialData`.
  - Warning: Critical error equivalent to summarization.

## 6. Style Components

ID: GUIDE-STS-COMPONENTS-01
Concept: Two levels of composition.

- Reference: GUIDE-STS-MICRO-01. Context: Micro-structure (individual line).
- Reference: GUIDE-STS-MACRO-01. Context: Macro-structure (document organization).

### 5.1. Micro-structure: The Telegraphic Line

ID: GUIDE-STS-MICRO-01
Definition: Atomic unit of information.
Requirement: Preserve every original data point.

- Model: `Keyword: EssentialData`
  - Keyword:
    - Definition: Word that defines the nature of the data.
    - Source: Must be an official keyword from the lexicon. Reference: GUIDE-STS-LEXICON-TABLE-01.
    - Example: `Objective:`, `Cause:`, `Requirement:`, `Condition:`.
  - EssentialData:
    - Definition: Pure information, stripped of verbosity.
    - Warning: Stripping verbosity is NOT summarizing or omitting.
    - Requirement: If the original data is a list of 5 items, all 5 items must be present.

- Process: Intention Translation
  - ID: GUIDE-STS-MICRO-TRANSLATION-01
  - Mechanism: Convert nuances of human language into explicit `Keywords`.
  - Example: `human: "Don't forget to..."` -> `telegraphic: Requirement:`
  - Example: `human: "It would be good to consider..."` -> `telegraphic: Recommendation:`
  - Example: `human: "This happens because..."` -> `telegraphic: Cause:`

### 5.2. Macro-structure: The Knowledge Network

ID: GUIDE-STS-MACRO-01
Purpose: Make knowledge navigable and contextual.
Concept: Three key structural elements.

- Concept: Header Hierarchy (`#`, `##`, `###`).
- Concept: Unique Identifiers (`ID:`). Reference: GUIDE-STS-ID-STANDARD-01.
- Concept: Cross-References (`Reference:`).

### 5.3. Composite Structures: Tables and Lists

ID: GUIDE-STS-STRUCTURES-01
Requirement: Grouping structures (tables, lists) must maintain their original format.
Justification: Preserving the inherent relationships of data is part of the `meat`.

- Concept: Tables (Markdown)
  - Requirement: Maintain intact table structure (`|...|...|`).
  - Prohibition: Converting a table to another format.
  - Action: Translate the content of EACH CELL into STS format.
  - Warning: Breaking the table is a loss of information.

- Concept: Lists (Ordered/Unordered)
  - Requirement: Maintain list format (`-` or `1.`).
  - Action: Translate each item into one or more STS lines.
  - Instruction: See list handling techniques. Reference: GUIDE-STS-METHODOLOGY-PHASE2-STRUCTURES-01.

### 5.4. Embedded Blocks: Artifact Containment Principle

ID: GUIDE-STS-COMPONENTS-EMBEDDED-BLOCK-01
Purpose: Define a formal mechanism to include artifacts governed by other standards within an STS document, without compromising the integrity of any standard.
Foundation: Artifact Containment Principle. An STS document can act as a high-level "container".
Model:

- Concept: Block Syntax.

`BEGIN_EMBEDDED_BLOCK:: <BLOCK_TYPE> <BLOCK_ID>`

```plain
... embedded artifact content ...
```

`END_EMBEDDED_BLOCK:: <BLOCK_ID>`

- Concept: Directive Components.
  - `BEGIN_EMBEDDED_BLOCK::`. Definition: Opening directive. On its own line, before the fenced block. Instructs parsers to prepare for a new parsing context.
  - `<BLOCK_TYPE>`. Requirement: Mandatory. The `ID:` of the guide document that governs the block's content (e.g., `GUIDE-SFD-STS-MASTER-01`).
  - `<BLOCK_ID>`. Requirement: Mandatory. A unique identifier for this block instance.
  - `Fenced Block (```)`. Definition: Standard Markdown code fence. It isolates the embedded artifact's content, preventing it from interfering with the parent STS document's rendering.
  - `END_EMBEDDED_BLOCK::`. Definition: Closing directive. On its own line, after the fenced block. Resumes normal STS processing.
- Requirement: The content within the block must be 100% compliant with the standard defined in `<BLOCK_TYPE>`.
- Prohibition: Mixing STS syntax within an embedded block.

## 7. Application Methodology

ID: GUIDE-STS-METHODOLOGY-01
Nature: Iterative cycle (architecture -> population -> connection -> audit) for the creation and validation of STS artifacts.
Requirement: Full understanding of the principles and components of this standard. Reference: GUIDE-STS-PRINCIPLES-01.

### Phase 1: Architecture

ID: GUIDE-STS-METHODOLOGY-PHASE1-01
Objective: Create the optimal logical skeleton for the knowledge.

- Process:
  1. Original `Meat` Analysis:
      - Action: Inventory the `meat` of the source text.
  2. Trunk Design (Central Idea):
      - Action: Define the fundamental `Purpose:` of the artifact.
  3. Main Branches Design (Macro-themes):
      - Action: Group `meat` into 3-7 thematic/functional areas.
      - Requirement: Themes must be mutually exclusive, collectively exhaustive.
  4. Secondary Branches and Leaves Design (Micro-themes):
      - Action: Break down each main branch into sub-themes and data.
  5. Assign Unique IDs:
      - Action: Assign a unique and descriptive `ID:` to EVERY NODE in the tree.
      - Requirement: ID must be unique across the entire knowledge base. Reference: GUIDE-STS-ID-STANDARD-01.

### Phase 2: Meat

ID: GUIDE-STS-METHODOLOGY-PHASE2-01
Requirement: Well-defined skeleton from Phase 1.
Action: Transfer all `meat` from the original doc to the new `skeleton`. Distill text into telegraphic format.

- Process:
  1. Eliminate Linguistic Fat:
      - Action: Discard words with no informational value (connectors, rhetoric, etc.).
  2. Convert to `Keyword: EssentialData` format:
      - Action: Identify the core idea of the sentence and choose the `Keyword` from the lexicon.
  3. Handling Composite Structures:
      - ID: GUIDE-STS-METHODOLOGY-PHASE2-STRUCTURES-01
      - Requirement: Preserve original format (table/list). Translate content to STS. Reference: GUIDE-STS-STRUCTURES-01.
      - Instruction: For list items requiring multiple STS lines, use nested sub-lists.
      - Warning: Creating numbered or sequenced Keywords is a critical anti-pattern. Reference: GUIDE-STS-LEXICON-ANTIPATTERNS-01.

### Phase 3: Nervous System

ID: GUIDE-STS-METHODOLOGY-PHASE3-01
Purpose: Transform static skeleton -> dynamic knowledge network.
Mechanism: Connect nodes (`ID`) with references (`Reference`).
Foundation: Rigorous application of the Single Source of Truth Principle. Reference: GUIDE-STS-PRINCIPLE-DUPLICATION-01.

- Process:
  1. Verify uniqueness of all IDs.
  2. Add Cross-References (`Reference:`) to eliminate `meat` duplication.

### Phase 4: Compliance Audit

ID: GUIDE-STS-METHODOLOGY-PHASE4-01
Instruction: Use this checklist for all STS standard compliance audits. It is a cyclical quality control, not a final step.
Condition: For an artifact to be considered compliant, all points must be approved.

Process: Audit-Checklist.

- [ ] Metadata Block: Is it present and complete? Reference: GUIDE-STS-METADATA-01.
- [ ] IDs and Hierarchy: Are IDs unique and compliant with the standard? Reference: GUIDE-STS-ID-STANDARD-01.
- [ ] Lexicon and Anti-Patterns: Is the canonical lexicon used and are anti-patterns avoided? Reference: GUIDE-STS-LEXICON-CONSOLIDATION-01.
- [ ] Absolute Fidelity (`Meat`): Is there a guarantee of zero summarization or omission compared to the source?
- [ ] Zero Duplication (`Reference:`): Is `Reference:` used consistently to avoid repeating information?
- [ ] Zero Fat: Has all linguistic and formatting fat (e.g., `...`) been eliminated?
- [ ] Language Invariance (Content): Is all `EssentialData` in the original source language, without translation? Reference: GUIDE-STS-PRINCIPLE-TRANSLATION-01.

## 8. Lexicon Governance

ID: GUIDE-STS-LEXICON-01
Concept: The use of canonical keywords is key but requires strict governance.
Warning: Anarchic use introduces ambiguity and destroys the knowledge base.

### 8.1. Governance Rules

ID: GUIDE-STS-LEXICON-GOVERNANCE-01

1. Requirement: This section is the single source of truth for keywords.
2. Prohibition: Creating terms outside this lexicon is a critical error.
3. Requirement: The use of the lexicon defined here is mandatory.
4. Concept: Lexicon Language vs. Content Language.
    - Foundation: The principle of Language Invariance is absolute. Reference: GUIDE-STS-PRINCIPLE-TRANSLATION-01.
    - Requirement: The `Keywords` lexicon is a fixed control vocabulary based on English.
    - Requirement: The `EssentialData` MUST remain in the original language of the source document.
    - Example: For a text in Spanish, the line would be `Purpose: Crear una serie de tutoriales en video.`.

### 8.2. Consolidated Lexicon

ID: GUIDE-STS-LEXICON-TABLE-01
Foundation: Specificity should reside in the `EssentialData`, not in the `Keyword`.
Req: The use of `Abbr.` is only valid if `STS-Directive: Lexicon-Mode = Abbreviated` is declared.

|Abbr.|Keyword|Usage Notes & Consolidation Guidelines|
|-|-|-|
|`Act:`|`Action:`|Use for: Concrete steps or actions to be taken.|
|`Warn:`|`Warning:`|Use for: Highlighting risks, critical information, or potential errors.|
|`Cause:`|`Cause:`|Use for: Explaining the reason or origin of a situation.|
|`Cpt:`|`Concept:`|Use for: Defining a concept or idea. Replaces: `Conclusion`, `Premise`, `Implication`, `Classification`, `Types`, `Scope`.|
|`Cond:`|`Condition:`|Use for: All types of conditions or prerequisites. Replaces: `Legal-Cond`.|
|`Ctx:`|`Context:`|Use for: Providing background, situational information, or scope. Replaces: `Note`, `Version`, `Update-Date`.|
|`Def:`|`Definition:`|Use for: Providing a formal definition.|
|`Dep:`|`Dependency:`|Use for: Indicating that one item depends on another.|
|`Dest:`|`Destination:`|Use for: Specifying the target, audience, or recipient.|
|`Dln:`|`Deadline:`|Use for: Defined deadlines or time periods.|
|`Ex:`|`Example:`|Use for: Providing a specific example.|
|`Fnd:`|`Foundation:`|Use for: The basis, legal, or theoretical backing of a statement. Replaces: `Reg-Framework`, `Norm-Basis`, `Legal-Ref`.|
|`ID:`|`ID:`|Standard. Represents the unique identifier. Abbreviation is the same as the full term.|
|`Instr:`|`Instruction:`|Use for: Giving a direct command or instruction.|
|`Just:`|`Justification:`|Use for: Providing the rationale or justification for an action or decision.|
|`Mech:`|`Mechanism:`|Use for: Describing how something works. Replaces: `Operationalization`, `Methodology`, `Platform`.|
|`Mssn:`|`Mission:`|Use for: Stating a high-level mission or purpose.|
|`Mdl:`|`Model:`|Use for: Describing a model, template, or structural example.|
|`Nat:`|`Nature:`|Use for: Describing the intrinsic quality or character of something.|
|`Obj:`|`Objective:`|Use for: Stating a specific, measurable objective. Replaces: `Doc-Goal`, `Aim`.|
|`Proc:`|`Process:`|Use for: Describing a series of steps or a process. Replaces: `Bi-phasic-Process`, `Op-Instrument`.|
|`Prohib:`|`Prohibition:`|Use for: All types of prohibitions and restrictions. Replaces: `Key-Restriction`, `Limitations`.|
|`Purp:`|`Purpose:`|Use for: Stating the purpose or intention. Replaces: `Exclusive-Purpose`.|
|`Rec:`|`Recommendation:`|Use for: Providing a recommendation or suggestion.|
|`Ref:`|`Reference:`|Standard. Represents a cross-reference to another ID. Abbreviation is the same as the full term.|
|`Req:`|`Requirement:`|Use for: All types of requirements. Replaces: `Pre-Req`, `General-Req`, `Critical-Req`, `Mandate`, `Compliance`.|
|`Res:`|`Result:`|Use for: Describing an outcome, result, or benefit. Replaces: `Expected-Outcome`, `Benefits`, `Product`.|
|`Resp:`|`Responsible:`|Use for: Assigning responsibility to an actor, role, or entity. Replaces: `GORE-Function`, `Gov-Attribute`, `Eval-Body`.|
|`Src:`|`Source:`|Use for: Citing the origin of information or a document. Replaces: `Primary-Legal-Basis`, `Key-Regulation`.|

### 8.3. Lexicon Extension Process

ID: GUIDE-STS-LEXICON-EXTENSION-01
Foundation: Allow for controlled growth of the lexicon without compromising consistency.
Requirement: Unilateral extension is prohibited. Any addition must follow this process.

- Process:
  1. Needs Validation: Demonstrate that the current lexicon is insufficient.
  2. Formal Proposal: Submit a request (term, definition, justification, example) to the standard's custodian.
  3. Centralized Review and Approval: The custodian evaluates the proposal.
  4. Canon Update: If approved, the custodian updates this guide. The term is only valid after the update.

### 8.4. Critical Anti-Pattern: Sequenced Keywords

ID: GUIDE-STS-LEXICON-ANTIPATTERNS-01

- Concept: Anti-Pattern. Definition: Suffixing canonical `Keywords` with numbers or letters (e.g., `Requirement-1:`, `Action-A:`, `Condition-2:`).
- Justification: This practice is a critical error. It makes the `Keyword` non-canonical, breaking parsers and searches. It conflates the *identity* of the information (the `Keyword`) with its *order* in a list, which should be handled by structure (lists), not by modifying the term itself. The order is structural `meat`, not lexical `meat`.
- Instruction: To express a list of items of the same type, use a standard Markdown list (`-`), where each list item begins with the same, unmodified canonical `Keyword`.
- Concept: Incorrect Example
  - `Requirement-1: The user must be authenticated.`
  - `Requirement-2: The password must be complex.`
- Concept: Correct Example
  - `- Requirement: The user must be authenticated.`
  - `- Requirement: The password must be complex.`

## 9. Application Examples

ID: GUIDE-STS-EXAMPLES-01

### 9.1. Transcription Example (English to STS)

ID: GUIDE-STS-EXAMPLE-EN-01

#### Human Text (English)
>
> "For our new content marketing strategy, which is detailed in the marketing plan, we propose creating a series of video tutorials. We believe this is essential because our latest survey revealed that 75% of users prefer this format. However, we must not forget that this will depend on the approved marketing budget, which is described in the financial document."

#### STS Transcription

```md
### Content Strategy

ID: EX-MKT-CONTENTS-01
Context: Marketing Plan. Reference: PLAN-MKT-GENERAL-01

- Purpose: Create a series of video tutorials.
- Justification: Survey reveals 75% of users prefer video format.
- Dependency: Budget approval. Reference: FIN-BUDGET-MKT-01.
```

### 9.2. Table Example

ID: GUIDE-STS-EXAMPLE-TABLE-01

#### STS Transcription

|Feature|Option A: On-Premise Server|Option B: Cloud SaaS|
|-|-|-|
|Initial Cost|Requirement: High initial investment (hardware, license purchase).|Model: Subscription (monthly/annual). Context: Low initial cost.|
|Maintenance|Responsible: Internal IT team (incl. updates, patches).|Responsible: Service provider.|
|Scalability|Mechanism: Purchase of additional hardware. Process: Slow, costly.|Mechanism: Subscription plan adjustment. Process: Instantaneous.|

### 9.3. Example Analysis

ID: GUIDE-STS-ANALYSIS-EXAMPLES-01
Result:

- Concept: Efficiency. Definition: Significant token reduction.
- Concept: Clarity. Definition: Use of explicit `Keywords` eliminates ambiguity.
- Concept: Fidelity. Definition: All original `meat` is preserved.
