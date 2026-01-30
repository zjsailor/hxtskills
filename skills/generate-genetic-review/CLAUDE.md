# Adaptive Genetic Review Writing Guidelines (CLAUDE.md)

## Overview
This document provides guidelines for writing adaptive genetic literature reviews that adjust their approach based on three distinct review archetypes:
- **Type A (Paradigm/Ethics)**: Policy, Ethics, New Standards
- **Type B (Clinical Management)**: Screening, Guidelines, Practice
- **Type C (Precision Mechanism)**: Genetics, Rare Disease, Targets

The review should adapt its focus, tone, and content structure based on the selected archetype while maintaining scientific rigor and integrating references from provided PDFs via Google NotebookLM.

## Review Type Selection

### Type A: Paradigm & Decision (Policy/Ethics Focus)
* **Reference Paradigm**: PES/PGT-P综述 [PMC11369226]
* **Appropriate For**: New technology controversies, ethics discussions, policy development, establishing new standards
* **Core Output**: Stakeholder analysis table, benefit-risk assessment model, policy recommendations
* **Tone**: Critical, balanced, forward-looking
* **Focus**: Ethical implications, societal impact, policy considerations

### Type B: Clinical Management (Practice/Guidelines Focus)
* **Reference Paradigm**: BRCA Carriers综述 [PMC12758042]
* **Appropriate For**: Disease diagnosis/treatment guidelines, screening strategies, preventive interventions, clinical implementation barriers
* **Core Output**: Risk stratification algorithm, clinical management pathway, implementation barrier analysis
* **Tone**: Prescriptive, practical, evidence-based
* **Focus**: Clinical implementation, practice guidelines, outcome optimization

### Type C: Precision Medicine (Mechanism/Targets Focus)
* **Reference Paradigm**: CANDLE/SOD1-ALS综述 [PMC12744253]
* **Appropriate For**: Single-gene disorders, rare diseases, molecular mechanisms, targeted drug development
* **Core Output**: Genotype-phenotype association matrix, molecular pathway diagram, case-level systematic review
* **Tone**: Mechanistic, precise, analytical
* **Focus**: Molecular mechanisms, genotype-phenotype correlations, targeted therapies

## Universal Writing Standards

### Core Requirements
- **No Fluff**: Avoid polite conversational fillers; output high-density academic content
- **Citation Format**: Use `[n, Author, Year]` format strictly
- **Visual Logic**: For every mechanism/pathway discussed, provide Mermaid code or detailed figure caption
- **Key Points**: Every major section starts with 3-5 bullet summary
- Every claim needs citation support
- Maintain consistent terminology throughout the manuscript
- Use proper genetic nomenclature and statistical reporting standards

### Structure Requirements
1. Title: Should reflect scope and type of review
2. Key Points: 3-5 bullets summarizing main findings (for each major section in Type A/B/C)
3. Abstract: 250-300 words, structured format
4. Introduction: Establish context appropriate to selected type
5. Methods: Literature search strategy and data extraction
6. Results: With type-appropriate data summary tables and figures
7. Main sections: Organized by type-specific focus
8. Discussion: Type-specific implications and considerations
9. Conclusion: Summary of findings and type-specific recommendations
10. Figures and Tables: Detailed descriptions with type-appropriate content
11. References: 30-80 high-quality sources (from databases and PDFs)

### Language Guidelines
- Use active voice where appropriate
- Define technical terms upon first use
- Maintain consistency in terminology
- Include hedging language for preliminary findings
- Balance technical precision with accessibility
- Ensure proper attribution of PDF-derived content
- **Adapt tone to selected type**: Critical/forward-looking (A), Prescriptive/evidence-based (B), or Mechanistic/analytical (C)

## Sequential Writing Approach by Type

### Phase 1: Strategic Alignment
- Analyze user topic against Type A/B/C definitions
- Confirm mode: "Based on your topic, I recommend **Type [X]** strategy because..."
- Generate type-specific CLAUDE.md and IMPLEMENTATION_PLAN.md

### Phase 2: Targeted Literature Mining
- Execute type-specific search strategy
- Focus on type-appropriate databases and metrics
- Gather type-appropriate evidence

### Phase 3: Structural Blueprinting
- Create outline with type-specific headers
- Plan type-specific tables and figures
- Ensure all required elements are included

### Phase 4: High-Density Drafting
- Write section by section using type-appropriate tone and focus
- Integrate data with type-specific metrics and analysis
- Maintain consistency with selected type

### Phase 5: Visual Synthesis
- Create type-specific figures and tables
- Ensure visuals align with type focus
- Include detailed captions appropriate to type

### Phase 6: Final Polish
- Ensure wider implications section aligns with target audience
- Verify citation format and completeness
- Confirm type consistency throughout

## Type-Specific Writing Guidelines

### Type A Writing Guidelines
#### Structure
- Introduction: The Conflict/New Technology
- Technical Background
- Estimated Benefits (Models vs. Data)
- Harms & Limitations (Personal & Societal)
- Stakeholder Perspectives
- Policy Recommendations
- Discussion (Ethics, Equity, Cost-Benefit)

#### Content Focus
- Educational background for interdisciplinary readers
- Separate "theoretical benefits" from "real-world harms"
- Section on ethical concerns, equity, and cost
- Stakeholder analysis and perspectives

#### Data Presentation
- Matrix comparing "model predictions" vs. "clinical reality"
- Benefit-risk analysis tables
- Stakeholder attitude surveys
- Policy impact assessments

#### Statistical Focus
- Cost-effectiveness ratios: ICER = $X,XXX per QALY
- Risk ratios: RR = X.XX (95% CI: X.XX-X.XX)
- Net health benefit: NHB = X.XX at willingness-to-pay of $X,XXX

### Type B Writing Guidelines
#### Structure
- Introduction: Disease Burden
- Identification & Risk Assessment
- Surveillance Strategies (Imaging/Biomarkers)
- Risk Reduction (Medical/Surgical)
- Implementation Barriers (The "Real World")
- Future: Personalized Prevention
- Discussion (Practice Gaps, Implementation Challenges)

#### Content Focus
- Clear risk identification and screening criteria
- Intervention hierarchy: surveillance → chemoprevention → surgery
- Explicit discussion of psychological, financial, and systemic barriers
- Clinical outcome optimization

#### Data Presentation
- "Clinical Management Recommendations" with evidence levels (A/B/C)
- Risk stratification algorithms
- Outcome measurement data
- Implementation rate statistics

#### Statistical Focus
- Odds ratios: OR = X.XX (95% CI: X.XX-X.XX, P<0.05)
- Effect sizes: Cohen's d = X.XX
- P-values: P<0.001, P=0.045 (not P<0.05)
- Allele frequencies: 0.XX (X%)

### Type C Writing Guidelines
#### Structure
- Introduction: Clinical Phenotype
- Genetic Architecture (Mutational Spectrum)
- Molecular Pathogenesis (The Pathway)
- Genotype-Phenotype Correlations
- Emerging Targeted Therapies
- Discussion (From Bench to Bedside)

#### Content Focus
- Detailed genetic basis and mutation types
- In-depth molecular pathway analysis
- Mechanism-based therapeutic approaches
- Case-level systematic review

#### Data Presentation
- Genotype-phenotype association matrix
- Molecular pathway diagrams
- Case-level synthesis data
- Functional annotation tables

#### Statistical Focus
- Expression levels: fold-change X.XX (P<0.05)
- Binding affinity: Kd = X.XX μM
- Pathway activity: normalized to control = X.XX ± X.XX

## Key Terminology

### Essential Genetic Terms
- **Allele**: Alternative form of a gene
- **Genotype**: Genetic makeup of an organism
- **Phenotype**: Observable characteristics
- **Penetrance**: Proportion expressing the associated trait
- **Expressivity**: Range of phenotypic expression
- **Haplotype**: Combination of alleles at multiple loci
- **Linkage Disequilibrium**: Non-random association of alleles

### Statistical Measures
- **Odds Ratio (OR)**: Measure of association between exposure and outcome
- **Relative Risk (RR)**: Ratio of risk in exposed vs. unexposed
- **P-value**: Probability of observing results by chance
- **Effect Size**: Magnitude of the relationship between variables
- **Confidence Interval**: Range likely to contain true value

### Genetic Technologies
- **WGS**: Whole Genome Sequencing
- **WES**: Whole Exome Sequencing
- **GWAS**: Genome-Wide Association Study
- **RNA-seq**: RNA Sequencing
- **ChIP-seq**: Chromatin Immunoprecipitation Sequencing
- **CRISPR**: Clustered Regularly Interspaced Short Palindromic Repeats

## Type-Specific Section Guidelines

### Type A Section Guidelines
#### Introduction
- Present the technological or policy conflict
- Establish the need for ethical consideration
- Define scope in terms of stakeholder impact

#### Discussion
- Focus on ethical implications
- Address equity and access concerns
- Analyze cost-benefit considerations
- Discuss regulatory frameworks

### Type B Section Guidelines
#### Introduction
- Establish disease burden and clinical significance
- Define the clinical management challenge
- State the scope in terms of patient outcomes

#### Discussion
- Focus on clinical practice gaps
- Address implementation challenges
- Analyze barrier intervention effectiveness
- Discuss outcome optimization

### Type C Section Guidelines
#### Introduction
- Present the clinical phenotype and molecular challenge
- Establish the need for mechanistic understanding
- Define scope in terms of molecular insights

#### Discussion
- Focus on molecular insights
- Address genotype-phenotype correlations
- Analyze therapeutic targeting precision
- Discuss bench-to-bedside translation

## PDF Integration Guidelines

### Processing with Google NotebookLM
- Upload PDFs in supported formats (PDF, DOCX, TXT, HTML)
- Extract key references and citations
- Identify important data points and statistics
- Summarize key findings
- Create REFERENCES_PDF.md and DATA_SUMMARY.md files

### Incorporating PDF Content
- Properly cite all PDF-derived content
- Integrate data points into type-appropriate summary tables
- Reference findings from PDFs alongside literature
- Maintain consistent terminology between literature and PDF sources
- Verify accuracy of extracted data

### Citation Format for PDF Sources
- Follow standard academic citation format
- Include specific page numbers when referencing direct quotes
- Clearly indicate when citing data from provided PDFs
- Maintain consistent citation style throughout

## Quality Criteria by Type

### Type A Quality Criteria
- Critical evaluation of policy implications
- Assessment of stakeholder bias in evidence
- Address ethical frameworks
- Discuss equity and access considerations
- Analyze cost-effectiveness methodologies

### Type B Quality Criteria
- Critical evaluation of clinical trial quality
- Assessment of implementation feasibility
- Address practice gap analysis
- Discuss barrier intervention effectiveness
- Evaluate clinical outcome measures

### Type C Quality Criteria
- Critical evaluation of mechanistic studies
- Assess genotype-phenotype correlation strength
- Address functional annotation accuracy
- Discuss therapeutic targeting precision
- Analyze molecular pathway validity

## Writing Tips

### Effective Paragraph Structure
1. Topic sentence introducing main point
2. Evidence supporting the point with citations
3. Critical analysis of the evidence
4. Transition to next point

### Citation Strategy
- Prioritize high-impact journals and recent publications
- Include landmark studies establishing foundational knowledge
- Balance methodological diversity
- Ensure representation of diverse populations
- Properly integrate citations from provided PDFs
- Match citation focus to selected type (policy studies for Type A, clinical trials for Type B, mechanistic studies for Type C)

### Figure and Table Ideas by Type

#### Type A Visuals
- Benefit-Risk Balance Scale
- Stakeholder Perspective Web
- Policy Impact Timeline
- Ethical Framework Comparison

#### Type B Visuals
- Clinical Decision Algorithm (Flowchart)
- Risk Stratification Matrix
- Implementation Barrier Analysis
- Outcome Optimization Pathway

#### Type C Visuals
- Molecular Signaling Pathway (Mechanism Diagram)
- Genotype-Phenotype Correlation Map
- Case-Level Synthesis Summary
- Therapeutic Targeting Network

## Common Pitfalls to Avoid
- Selecting wrong review type for the research question
- Mixing approaches from different types inconsistently
- Failing to adapt tone to selected type
- Neglecting type-specific required elements
- Improper citation of PDF-derived content
- Failure to verify accuracy of NotebookLM-extracted data
- Unequal integration of literature vs. PDF content
- Not maintaining type-specific focus throughout