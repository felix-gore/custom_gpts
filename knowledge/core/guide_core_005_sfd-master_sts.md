# Master Guide: Structured Form Definition (SFD) in STS format

ID: GUIDE-SFD-STS-MASTER-01
Version: 1.0.1
Status: Published
Human-Creator: FS
Human-Editor: FS
Model-Collaborator: IA-GEMINI
Creation-Date: 2025-06-28
Modification-Date: 2025-07-06
Primary-Source: GUIDE-SFD-MASTER-01
Ref-STS-Guide: GUIDE-STS-MASTER-01

## 1. Philosophy and Purpose

ID: GUIDE-SFD-STS-PHILOSOPHY-01
Mssn: Govern transcription of forms and rigidly structured docs into high-fidelity knowledge artifacts.
Dest: LLM processing for analysis, automated completion, user guidance, validation.
Rel: SFD is a standard complementary and separate from Structured Telegraphic Style (STS).
Fnd: SFD is a specialized component of the ALM Coherence Stack, essential for agents with structured data interaction capabilities. Ref: `guide_core_002_alm-master_sts.md`.

- Ctx: STS refactors unstructured/semi-structured prose.
- Ctx: SFD deconstructs/refactors artifacts defined by rigid structure, functional metadata, interaction logic (i.e., forms).
Purp: Capture not only "what" (field labels) but "how" (rules, types, constraints, options, conditional logic).
Fnd: The Principle of Functional Fidelity.
Cpt: Functional-Fidelity.
- Def: Complete, lossless preservation of a form's original structure, metadata, validation rules, and conditional logic.
Warn: SFD transcription is not a summary; it is a functional re-architecture.
Res: Loss of a single validation rule is a critical failure.
Cpt: Usage-Model. Def: An SFD artifact can be used standalone or embedded within an STS document using the `EMBEDDED_BLOCK` directive. Ref: GUIDE-STS-MASTER-01.

## 2. Fundamental Principles

ID: GUIDE-SFD-STS-PRINCIPLES-01

### Principle-1: Functional Fidelity (Zero Abstraction)

ID: GUIDE-SFD-STS-PRINCIPLE-FIDELITY-01
Req: Transcribe every rule, constraint, option, and instruction from original form.
Warn: Abstracting or omitting functional details corrupts the artifact's utility for validation or interaction.

### Principle-2: Structure is Meaning

ID: GUIDE-SFD-STS-PRINCIPLE-STRUCTURE-01
Cpt: Form hierarchy (sections, groups, fields) is informational `meat`, not formatting.
Act: Represent hierarchy via Markdown headers (`###`, `####`) and unique `ID:` tags.
Prohib: Implicit representation of structure.

### Principle-3: Explicit Semantics (Zero Ambiguity)

ID: GUIDE-SFD-STS-PRINCIPLE-SEMANTICS-01
Req: Define every characteristic of a form element with a unique `KeyTerm` from the official SFD Lexicon.
Just: Guarantees unambiguous machine parsing by an LLM.

### Principle-4: LLM-First Design (Maximum Parsability)

ID: GUIDE-SFD-STS-PRINCIPLE-LLM-FIRST-01
Purp: Syntax designed for easy, reliable machine parsing.
Cpt: Predictable block structure and controlled vocabularies ensure model can convert SFD to a structured object (e.g., JSON) with perfect accuracy.

## 3. Architectural Components

ID: GUIDE-SFD-STS-COMPONENTS-01
Req: An SFD artifact is a hierarchy of three primary components.

- Cpt: Form-Artifact.
  - Def: Entire SFD document, representing a single, complete form. Begins with control metadata block.
- Cpt: Form-Section.
  - Def: Logical grouping of fields, represented by `###` header. Corresponds to `<fieldset>` or visually distinct section.
- Cpt: Form-Field.
  - Def: Atomic unit of information. Represents a single input, label, or interactive element. Each is a block of `KeyTerm: Value` pairs under a `####` header.

## 4. The Form-Field Component & Lexicon

ID: GUIDE-SFD-STS-FIELD-COMPONENT-01
Purp: Exhaustively describe a single form element using a mandatory, controlled lexicon.
Mdl: Each `Form-Field` is a block of key-value pairs.

```markdown
#### Field's Human-Readable Name
ID: FORM-ID-SECTION-FIELD-01
Field-Label: "Applicant Full Name"
Field-Type: Text
Field-Instr: "Please enter your first name and surname."
Field-Constraint: "Req: mandatory. Max-Len: 150."
Field-Placeholder: "e.g., Jane Doe"
```

### 4.1. SFD Canonical Lexicon

ID: GUIDE-SFD-STS-LEXICON-01
Req: Use of this lexicon is mandatory for defining `Form-Field` components.

|KeyTerm|Mandatory|Definition (`Def:`) & Usage|
|-|-|-|
|`ID:`|Yes|Def: Unique identifier for a `Form-Section` or `Form-Field`.|
|`Field-Label:`|Yes|Def: Visible text label associated with the field.|
|`Field-Type:`|Yes|Def: Data type or control type. Req: Must use controlled vocabulary.|
|`Field-Instr:`|No|Def: Specific user instructions for filling out the field.|
|`Field-Constraint:`|No|Def: Validation rules applied to the field's value. Req: Uses constraint mini-language.|
|`Field-Placeholder:`|No|Def: Example text that appears inside an empty field.|
|`Field-Option:`|Conditional|Def: One line per available choice. Req: For `Radio`, `Select`, `Checkbox-Group`.|
|`Field-Logic:`|No|Def: Conditional visibility or requirements based on other fields.|
|`Field-Group:`|No|Def: A sub-header for grouping multiple `Field-Option`s.|

### 4.2. Controlled Vocabulary for `Field-Type`

ID: GUIDE-SFD-STS-LEXICON-FIELD-TYPE-01
Req: Use ONLY the following values for `Field-Type:`.
Just: Controlled vocabulary is critical for the LLM to understand a field's interaction model.

- `Text`: Single-line text input.
- `TextArea`: Multi-line text input.
- `Number`: Numerical input (integer or decimal).
- `Date`: Date input.
- `Checkbox`: Single, standalone checkbox.
- `Checkbox-Group`: Set of related checkboxes (multiple selections allowed).
- `Radio`: Group of option buttons (single selection only).
- `Select`: Dropdown list (single or multiple selections).
- `File`: Control for file uploads.
- `Static-Text`: Non-editable text block (e.g., instruction paragraph, warning).
- `Repeater`: Complex type defining a section of fields that can be dynamically duplicated.

### 4.3. Mini-Language for `Field-Constraint`

ID: GUIDE-SFD-STS-LEXICON-CONSTRAINT-01
Mdl: Constraints are a period-separated list of rules.
Ex: `Field-Constraint: "Req: mandatory. Max-Len: 50. Format: email."`

- `Req: mandatory` / `Req: optional`
- `Max-Len: <number>` (for text)
- `Min-Len: <number>` (for text)
- `Max-Val: <number>` (for numbers/dates)
- `Min-Val: <number>` (for numbers/dates)
- `Format: <type>` (e.g., `email`, `url`, `YYYY-MM-DD`, `alphanumeric`)
- `Pattern: <regex>` (for complex text validation)
- `Max-Selections: <number>` (for multi-select fields)

## 5. Application Methodology

ID: GUIDE-SFD-STS-METHODOLOGY-01
Proc: 4-phase cycle to convert any form into a compliant SFD artifact.

### Phase 1: Architectural Deconstruction

ID: GUIDE-SFD-STS-METHODOLOGY-PHASE1-01
Act: Perform visual and logical analysis of the source form.

- Proc-1: Inventory-Sections. Identify all logical groupings or sections.
- Proc-2: Inventory-Fields. For each section, list every label, input field, instruction, and visible validation rule.

### Phase 2: Atomic Transcription

ID: GUIDE-SFD-STS-METHODOLOGY-PHASE2-01
Act: Convert each identified form element into a `Form-Field` block.

- Proc-1: Assign-Core. For each field, create a `####` block and assign `ID:` and `Field-Label:`.
- Proc-2: Assign-Type. Assign the correct `Field-Type:` from the controlled vocabulary.
- Proc-3: Assign-Details. Add `Field-Instr:`, `Field-Constraint:`, `Field-Placeholder:` as they appear in the source.
- Proc-4: Assign-Options. For `Radio`, `Select`, `Checkbox-Group`, add each choice as a separate `Field-Option:` line.

### Phase 3: Hierarchical Assembly

ID: GUIDE-SFD-STS-METHODOLOGY-PHASE3-01
Act: Assemble atomic `Form-Field` blocks into the final artifact.

- Proc-1: Group. Arrange `Form-Field` blocks under their corresponding `Form-Section` (`###`) headers.
- Proc-2: Identify. Ensure every `Form-Section` and `Form-Field` has a unique, descriptive `ID:`.
- Proc-3: Add-Metadata. Prepend the SFD Control Metadata Block to the top of the file.

### Phase 4: Logic & Connection Layer

ID: GUIDE-SFD-STS-METHODOLOGY-PHASE4-01
Act: Encode interdependencies between fields.

- Proc-1: Analyze-Logic. Identify all conditional rules (e.g., "If checkbox A is checked, field B becomes mandatory").
- Proc-2: Implement-Logic. Use the `Field-Logic:` key to describe the rules, referencing other fields by their `ID:`.
- Ex: `Field-Logic: "Cond: (Ref: FORM-ID-CHECKBOX-A.Value == 'true') -> Req: mandatory. Visibility: show."`

## 6. Example of Application

ID: GUIDE-SFD-STS-EXAMPLE-01
Purp: The following `markdown` block is a canonical example of a final SFD artifact.

### Source Form (Conceptual)

> Section 1: Project Details
>
> Project Name: \[ Text input, required, max 200 chars ]
> *Please provide a descriptive name.*
>
> Project Type: \[ Dropdown: [Investment, Social, Cultural], required ]
>
> Section 2: Funding
>
> Amount Requested ($): \[ Numeric input, required ]
>
> Requires Legal Review?: \[ ☐ (Checkbox) ]
>
> Justification for Legal Review: \[ Text area, appears only if the previous checkbox is checked ]

### SFD Transcription

```markdown
# Project Funding Application Form
ID: FORM-PROJFUND-MASTER-01
Version: 1.0.0
Status: Published
Ref-SFD-Guide: GUIDE-SFD-MASTER-01

### Section 1: Project Details
ID: FORM-PROJFUND-S1-DETAILS-01

#### Project Name
ID: FORM-PROJFUND-S1-NAME-01
Field-Label: "Project Name"
Field-Type: Text
Field-Instr: "Please provide a descriptive name."
Field-Constraint: "Req: mandatory. Max-Len: 200."

#### Project Type
ID: FORM-PROJFUND-S1-TYPE-01
Field-Label: "Project Type"
Field-Type: Select
Field-Constraint: "Req: mandatory."
- Field-Option: "Investment"
- Field-Option: "Social"
- Field-Option: "Cultural"

### Section 2: Funding
ID: FORM-PROJFUND-S2-FUNDING-01

#### Amount Requested
ID: FORM-PROJFUND-S2-AMOUNT-01
Field-Label: "Amount Requested ($)"
Field-Type: Number
Field-Constraint: "Req: mandatory. Min-Val: 0."

#### Requires Legal Review
ID: FORM-PROJFUND-S2-LEGALREV-01
Field-Label: "Requires Legal Review?"
Field-Type: Checkbox

#### Justification for Legal Review
ID: FORM-PROJFUND-S2-JUSTIFY-01
Field-Label: "Justification for Legal Review"
Field-Type: TextArea
Field-Logic: "Cond: (Ref: FORM-PROJFUND-S2-LEGALREV-01.Value == 'true') -> Visibility: show. Req: mandatory."
Field-Constraint: "Req: optional."
```
