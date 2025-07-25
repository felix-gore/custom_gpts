# Master Guide: Structured Form Definition (SFD) in STS format

ID: GUIDE-SFD-STS-MASTER-01
Version: 6.0.0
Status: Published
Human-Creator: FS
Model-Collaborator: IA-GEMINI
Creation-Date: 2025-06-28
Modification-Date: 2025-07-24
Source: GUIDE-STS-MASTER-01

## 0. Meta-Commentary: How to Read This Document

ID: GUIDE-SFD-STS-META-01
Purp: Define the two perspectives for interpreting this guide.
Req: Understanding these perspectives is mandatory for correct application.

- Cpt: Authoring Perspective (For Humans).
  - Dest: Human developers who need to transcribe forms into SFD content blocks within a parent STS artifact.
  - Ctx: This perspective focuses on the prescriptive rules for creating SFD content (Sections 3, 5, 6, 7).

- Cpt: Parsing Perspective (For Machines).
  - Dest: AI Agents and LLMs that need to read, interpret, and reason over SFD content.
  - Ctx: SFD content is always encapsulated within a parent STS document. The AI MUST first apply the `LLM Parsing Instructions` from the parent document to identify an `EMBEDDED_BLOCK` of type `SFD`. Only then should it apply the specific SFD parsing rules defined in this guide.

## 1. Role and Relationship to STS

ID: GUIDE-SFD-STS-ROLE-01
Purp: Define SFD's position relative to the master STS standard.

- Cpt: SFD as an Extension.
  - Def: SFD is not a standalone document standard. It is a specialized content format.
  - Req: SFD content MUST always be encapsulated within an `EMBEDDED_BLOCK` inside a host STS document.
  - Src: GUIDE-STS-COMPONENTS-EMBEDDED-BLOCK-01.
- Cpt: Parsing Hierarchy.
  - Mech: An STS parser identifies an SFD block. A specialized SFD parser then processes the content of that block.
  - Warn: The keywords and structures defined in this SFD guide are ONLY valid inside an SFD `EMBEDDED_BLOCK`. They are not canonical STS keywords.

## 2. Philosophy and Purpose

ID: GUIDE-SFD-STS-PHILOSOPHY-01
Mssn: Govern transcription of forms and rigidly structured docs into high-fidelity knowledge artifacts.
Dest: LLM processing for analysis, automated completion, user guidance, validation.
Cpt: Functional-Fidelity.

- Def: Complete, lossless preservation of a form's original structure, metadata, validation rules, and conditional logic.
Warn: SFD transcription is not a summary; it is a functional re-architecture of a form into a structured, machine-readable format.

## 3. SFD Usage Model: Embedded Artifact

ID: GUIDE-SFD-STS-USAGE-MODEL-01
Purp: Define the single, mandatory context in which an SFD artifact can exist.

- Cpt: Embedded-Only Model.
  - Ctx: The SFD content is a component within a larger STS document that provides narrative or structural context. This is the only valid use case.
  - Req: The SFD content MUST be encapsulated within an `EMBEDDED_BLOCK` directive.
  - Mdl:
    - `BEGIN_EMBEDDED_BLOCK:: SFD FORM-UNIQUE-ID`
    - The SFD content starts immediately with `### Form-Section` headers.
    - It does NOT contain its own STS metadata or LLM instructions; it inherits them from the parent STS document.
    - `END_EMBEDDED_BLOCK:: FORM-UNIQUE-ID`
  - Src: GUIDE-STS-COMPONENTS-EMBEDDED-BLOCK-01.

## 4. Fundamental Principles

ID: GUIDE-SFD-STS-PRINCIPLES-01
Fnd: Aligned with STS principles for consistency. Src: GUIDE-STS-PRINCIPLES-01.

- Cpt: Absolute Fidelity (Principle 1).
  - ID: GUIDE-SFD-STS-PRINCIPLE-FIDELITY-01
  - Ctx: Inherited from STS (GUIDE-STS-PRINCIPLE-FIDELITY-01).
  - Req: Transcribe every rule, constraint, option, and instruction.
  - Warn: Abstracting or omitting functional details corrupts the artifact's utility.

- Cpt: Self-Contained Source of Truth (Principle 2).
  - ID: GUIDE-SFD-STS-PRINCIPLE-SSOT-01
  - Ctx: Inherited from STS (GUIDE-STS-PRINCIPLE-SSOT-01).
  - Req: Define every characteristic of a form element with a `KeyTerm` from the official SFD Lexicon.
  - Just: Guarantees unambiguous machine parsing.

- Cpt: Structure is Meaning (Principle 3).
  - ID: GUIDE-SFD-STS-PRINCIPLE-STRUCTURE-01
  - Ctx: Inherited from STS (GUIDE-STS-PRINCIPLE-STRUCTURE-01).
  - Cpt: Form hierarchy (sections, fields) is informational `meat`.
  - Act: Represent hierarchy via Markdown headers (`###`, `####`) and unique `ID:` tags.

- Cpt: Zero Fat and Maximum Density (Principle 4).
  - ID: GUIDE-SFD-STS-PRINCIPLE-DENSITY-01
  - Ctx: Inherited from STS (GUIDE-STS-PRINCIPLE-DENSITY-01).
  - Act: Radically eliminate filler words in form transcriptions, converting all meaning into SFD lexicon terms.

- Cpt: RAG Optimization (Principle 5).
  - ID: GUIDE-SFD-STS-PRINCIPLE-RAG-01
  - Ctx: Inherited from STS (GUIDE-STS-PRINCIPLE-RAG-01).
  - Req: Each `Form-Section` chunk must be informationally dense and as self-contained as possible.

- Cpt: Language Invariance (Principle 6).
  - ID: GUIDE-SFD-STS-PRINCIPLE-LANGUAGE-INVARIANCE-01
  - Ctx: Inherited from STS (GUIDE-STS-PRINCIPLE-LANGUAGE-INVARIANCE-01).
  - Fnd: SFD maintains the original language of form content.
  - Prohib: Translating `EssentialData` (labels, instructions, etc.).

## 5. Architectural Components

ID: GUIDE-SFD-STS-COMPONENTS-01
Req: An SFD artifact is a hierarchy of components.

- Cpt: Form-Section.
  - Def: Logical grouping of fields, represented by `###` header.
- Cpt: Form-Field.
  - Def: Atomic unit of information. Represents a single input, label, or interactive element. Each is a block of `KeyTerm: Value` pairs under a `####` header.

### 5.1. The Form-Field Component & SFD Lexicon

ID: GUIDE-SFD-STS-FIELD-COMPONENT-01
Purp: Exhaustively describe a single form element using a mandatory, controlled lexicon.
Mdl: Each `Form-Field` is a block of key-value pairs.
Req: Use of this lexicon is mandatory for defining `Form-Field` components.
Warn: The SFD Lexicon and its syntax (e.g., for `Field-Logic`) are only valid within an SFD `EMBEDDED_BLOCK`. They are not part of the canonical STS lexicon.

|KeyTerm|Mandatory|Definition (`Def:`) & Usage|
|-|-|-|
|`ID:`|Yes|Def: Unique identifier for a `Form-Section` or `Form-Field`. Follows STS `ID` standard. Src: GUIDE-STS-ID-STANDARD-01.|
|`Field-Label:`|Yes|Def: Visible text label associated with the field.|
|`Field-Type:`|Yes|Def: Data type or control type. Req: Must use controlled vocabulary. Src: GUIDE-SFD-STS-LEXICON-FIELD-TYPE-01.|
|`Field-Instr:`|No|Def: Specific user instructions for filling out the field.|
|`Field-Constraint:`|No|Def: Validation rules. Req: Uses constraint mini-language. Src: GUIDE-SFD-STS-LEXICON-CONSTRAINT-01.|
|`Field-Placeholder:`|No|Def: Example text that appears inside an empty field.|
|`Field-Option:`|Conditional|Def: One line per available choice. Req: For `Radio`, `Select`, `Checkbox-Group`.|
|`Field-Logic:`|No|Def: Conditional visibility or requirements based on other fields. Ctx: Uses a micro-syntax where `Ref:` points to another field's `ID` and can access its state (e.g., `.Value`).|
|`Field-Group:`|No|Def: A sub-header for grouping multiple `Field-Option`s.|

### 5.2. Controlled Vocabulary for `Field-Type`

ID: GUIDE-SFD-STS-LEXICON-FIELD-TYPE-01
Req: Use ONLY the following values for `Field-Type:`.

- `Text`, `TextArea`, `Number`, `Date`, `Checkbox`, `Checkbox-Group`, `Radio`, `Select`, `File`, `Static-Text`, `Repeater`.

### 5.3. Mini-Language for `Field-Constraint`

ID: GUIDE-SFD-STS-LEXICON-CONSTRAINT-01
Mdl: Constraints are a period-separated list of rules. Ex: `Field-Constraint: "Req: mandatory. Max-Len: 50."`

- `Req: mandatory` / `Req: optional`
- `Max-Len: <number>`, `Min-Len: <number>`
- `Max-Val: <number>`, `Min-Val: <number>`
- `Format: <type>` (e.g., `email`, `url`, `YYYY-MM-DD`)
- `Pattern: <regex>`

## 6. Application Methodology (For Authors)

ID: GUIDE-SFD-STS-METHODOLOGY-01
Nat: Iterative cycle (deconstruction -> transcription -> assembly -> connection -> audit).
Src: GUIDE-STS-METHODOLOGY-01.

- Proc: Phase 1: Deconstruction. Act: Analyze the source form, inventorying all sections and fields.
- Proc: Phase 2: Transcription. Act: Convert each form element into a `Form-Field` block using the SFD lexicon.
- Proc: Phase 3: Assembly. Act: Group `Form-Field` blocks under `Form-Section` headers and ensure unique `ID`s.
- Proc: Phase 4: Connection. Act: Encode inter-field dependencies using `Field-Logic:`.
- Proc: Phase 5: Compliance Audit. Act: Use the STS compliance checklist for all audits. Src: GUIDE-STS-METHODOLOGY-PHASE4-01.

## 7. Compliance

ID: GUIDE-SFD-STS-COMPLIANCE-01
Instr: Use STS compliance checklist for all audits.
Src: GUIDE-STS-METHODOLOGY-PHASE4-01.

## 8. Example of Application

ID: GUIDE-SFD-STS-EXAMPLE-01
Warn: The following content is strictly illustrative.
Ctx: This shows a form embedded within a larger STS document, which is the only correct use case.

```plain
# Project Analysis Document
ID: PLAN-PROJ-ANALYSIS-01
Version: 1.0.0
Status: Draft
...

### Section 3: Risk Assessment
ID: PLAN-PROJ-ANALYSIS-S3-RISK-01
Purp: Document the initial risk assessment for the project.
Fnd: A key risk is related to legal compliance, which must be formally declared.

BEGIN_EMBEDDED_BLOCK:: SFD RISK-DECLARATION-FORM-01

### Legal Compliance Declaration
ID: FORM-RISKDEC-S1-LEGAL-01

#### Requires Legal Review
ID: FORM-RISKDEC-S1-LEGALREV-01
Field-Label: "Requires Legal Review?"
Field-Type: Checkbox
Field-Constraint: "Req: mandatory."

#### Justification for Legal Review
ID: FORM-RISKDEC-S1-JUSTIFY-01
Field-Label: "Justification for Legal Review"
Field-Type: TextArea
Field-Logic: "Cond: (Ref: FORM-RISKDEC-S1-LEGALREV-01.Value == 'true') -> Req: mandatory."
Field-Constraint: "Req: optional."

END_EMBEDDED_BLOCK:: RISK-DECLARATION-FORM-01

### Section 4: Next Steps
ID: PLAN-PROJ-ANALYSIS-S4-NEXT-01
Act: Submit the declaration for formal review.
Dep: Completion of the form in RISK-DECLARATION-FORM-01.
```
