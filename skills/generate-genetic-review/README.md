# Adaptive Genetic Literature Review Generation Skill

This skill enables the systematic creation of comprehensive literature reviews for genetic research that adapt to three distinct archetypes based on the research purpose.

## Purpose
Generate high-quality, academic literature reviews focusing on:
- Genetic disorders and rare diseases
- Genomic sequencing technologies
- Inherited disorders
- Population genetics
- Genomic medicine
- Gene therapy and editing

Reviews adapt to one of three archetypes:
- **Type A (Paradigm/Ethics)**: Policy, Ethics, New Standards
- **Type B (Clinical Management)**: Screening, Guidelines, Practice
- **Type C (Precision Mechanism)**: Genetics, Rare Disease, Targets

## Scope
- 30-80 references
- 4000-8000 words
- Academic writing standards
- Clinical relevance
- Critical analysis
- Integration with Google NotebookLM for PDF processing
- Adaptive approach based on research purpose

## Key Features
- Adaptive review type selection (A/B/C) based on research purpose
- Systematic literature search strategy tailored to review type
- Structured manuscript organization with type-specific sections
- Genetic terminology standards
- Statistical reporting guidelines by type
- Quality assurance protocols
- Google NotebookLM integration for PDF processing
- Type-specific writing approach (Paradigm/Ethics, Clinical Management, or Precision Mechanism)
- Type-appropriate data summary tables and figures
- Proper citation of PDF-derived content

## Review Types

### Type A: Paradigm & Decision (Policy/Ethics Focus)
- **Reference Paradigm**: PES/PGT-P综述 [PMC11369226]
- **Appropriate For**: New technology controversies, ethics discussions, policy development, establishing new standards
- **Core Output**: Stakeholder analysis table, benefit-risk assessment model, policy recommendations
- **Tone**: Critical, balanced, forward-looking
- **Focus**: Ethical implications, societal impact, policy considerations

### Type B: Clinical Management (Practice/Guidelines Focus)
- **Reference Paradigm**: BRCA Carriers综述 [PMC12758042]
- **Appropriate For**: Disease diagnosis/treatment guidelines, screening strategies, preventive interventions, clinical implementation barriers
- **Core Output**: Risk stratification algorithm, clinical management pathway, implementation barrier analysis
- **Tone**: Prescriptive, practical, evidence-based
- **Focus**: Clinical implementation, practice guidelines, outcome optimization

### Type C: Precision Medicine (Mechanism/Targets Focus)
- **Reference Paradigm**: CANDLE/SOD1-ALS综述 [PMC12744253]
- **Appropriate For**: Single-gene disorders, rare diseases, molecular mechanisms, targeted drug development
- **Core Output**: Genotype-phenotype association matrix, molecular pathway diagram, case-level systematic review
- **Tone**: Mechanistic, precise, analytical
- **Focus**: Molecular mechanisms, genotype-phenotype correlations, targeted therapies

## PDF Integration
- Upload and process provided PDFs via Google NotebookLM
- Extract references and data from PDFs
- Integrate PDF findings with database literature
- Maintain proper citation standards for all sources
- Adapt PDF integration approach based on selected review type

## Sequential Writing Approach by Type
1. Strategic Alignment (Review Type Selection)
2. Targeted Literature Mining (Type-Specific Search)
3. Structural Blueprinting (Type-Specific Outline)
4. High-Density Drafting (Type-Appropriate Content)
5. Visual Synthesis (Type-Specific Figures and Tables)
6. Final Polish (Type-Consistent Review)

## Files Included
- `SKILL.md`: Main skill definition and adaptive guidelines
- `CLAUDE.md`: Type-specific writing guidelines and standards
- `IMPLEMENTATION_PLAN.md`: Step-by-step execution plan
- `WORKFLOW.md`: Phased systematic process by review type
- `DOMAINS.md`: Genetic research domain classifications
- `GLOSSARY.md`: Comprehensive genetic terminology
- `PDF_REFERENCES.md`: PDF integration and citation guide

## Usage
Trigger when requesting:
- Genetic literature reviews with specific focus requirements
- Rare disease surveys requiring policy/clinical/mechanistic focus
- Genomic medicine overviews with particular emphasis
- Gene therapy assessments with specific perspective
- Inherited disorder analyses with clinical/ethical/mechanistic focus