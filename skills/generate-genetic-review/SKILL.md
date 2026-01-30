---
name: adaptive-genetic-review
description: Generate high-impact genetic literature reviews adapting to three specific archetypes: Paradigm/Decision (Type A), Clinical Management (Type B), and Precision Mechanism (Type C). Use when writing survey papers, systematic reviews, or literature analyses on genetics topics that require specific review approaches. Triggers on requests for "genetic review", "rare disease review", "gene therapy survey", "genomic medicine literature review", or mentions of writing academic reviews on genetics, genomics, or inherited disorders with specific requirements. References in 30-80 range. Word count 4000-8000 words. Integrates with Google NotebookLM to read provided PDFs and cite their references.
allowed-tools:
  - Read
  - Write
  - Edit
  - Glob
  - Grep
  - Bash
  - WebSearch
  - WebFetch
  - TodoWrite
  - Exec
  - Image
---

# Adaptive Genetic Research Literature Review Writing Skill

An advanced systematic workflow for writing comprehensive literature reviews in genetic research, rare diseases, and genomic medicine that adapts to three distinct review archetypes based on the research purpose.

## Quick Start

When user requests a genetic literature review:

1. **Classify the review type** based on user's research purpose:
   - **Type A (Paradigm/Ethics)**: Policy, Ethics, New Standards
   - **Type B (Clinical Path)**: Screening, Guidelines, Practice
   - **Type C (Precision/Mech)**: Genetics, Rare Disease, Targets

2. **Initialize project** with core files:
   - `CLAUDE.md` - Writing guidelines and terminology
   - `IMPLEMENTATION_PLAN.md` - Staged execution plan
   - `manuscript_draft.md` - Main manuscript
   - `REFERENCES_PDF.md` - Extracted references from provided PDFs
   - `DATA_SUMMARY.md` - Summary of key data points from PDFs

3. **Follow the phased writing workflow** (see [WORKFLOW.md](WORKFLOW.md)):
   - Mode-specific initialization
   - Targeted literature mining
   - Structural blueprinting
   - High-density drafting
   - Visual synthesis
   - Final polish

4. **Integrate PDF sources** via Google NotebookLM (if provided)

## Review Types and Their Applications

### Type A: Paradigm & Decision (Policy/Ethics Focus)
* **Reference Paradigm**: PES/PGT-P综述 [PMC11369226]
* **Appropriate For**: New technology controversies, ethics discussions, policy development, establishing new standards
* **Core Output**: Stakeholder analysis table, benefit-risk assessment model, policy recommendations

### Type B: Clinical Management (Practice/Guidelines Focus)
* **Reference Paradigm**: BRCA Carriers综述 [PMC12758042]
* **Appropriate For**: Disease diagnosis/treatment guidelines, screening strategies, preventive interventions, clinical implementation barriers
* **Core Output**: Risk stratification algorithm, clinical management pathway, implementation barrier analysis

### Type C: Precision Medicine (Mechanism/Targets Focus)
* **Reference Paradigm**: CANDLE/SOD1-ALS综述 [PMC12744253]
* **Appropriate For**: Single-gene disorders, rare diseases, molecular mechanisms, targeted drug development
* **Core Output**: Genotype-phenotype association matrix, molecular pathway diagram, case-level systematic review

## Core Principles

### Writing Style by Type

#### Type A (Paradigm/Ethics)
- **Tone**: Critical, balanced, forward-looking
- **Structure**:
  - Educational background for interdisciplinary readers
  - Separate "theoretical benefits" from "real-world harms"
  - Section on ethical concerns, equity, and cost
- **Tables**: Matrix comparing "model predictions" vs. "clinical reality"

#### Type B (Clinical Management)
- **Tone**: Prescriptive, practical, evidence-based
- **Structure**:
  - Clear risk identification and screening criteria
  - Intervention hierarchy: surveillance → chemoprevention → surgery
  - Explicit discussion of psychological, financial, and systemic barriers
- **Tables**: "Clinical Management Recommendations" with evidence levels (A/B/C)

#### Type C (Precision Medicine)
- **Tone**: Mechanistic, precise, analytical
- **Structure**:
  - Detailed genetic basis and mutation types
  - In-depth molecular pathway analysis
  - Mechanism-based therapeutic approaches
- **Data Handling**: Perform "case-level synthesis" when possible (e.g., "Review of 50 reported cases showed...")

### Universal Requirements
- **No Fluff**: Avoid polite conversational fillers; output high-density academic content
- **Citation Format**: Use `[n, Author, Year]` format strictly
- **Visual Logic**: For every mechanism/pathway discussed, provide Mermaid code or detailed figure caption
- **Key Points**: Every major section starts with 3-5 bullet summary

### Required Elements
- **Mode-Specific Key Points box** (3-5 bullets) after title
- **Mode-Specific Comparison table** for each major section
- **Mode-Specific Metrics** with consistent format (statistics, ratios, or mechanisms)
- **Mode-Specific Figure placeholders** with detailed captions
- **Mode-Specific References organized by topic** (30-80 typical)

### Paragraph Structure
1. Topic sentence (main claim)
2. Supporting evidence (citations + data)
3. Analysis (critical evaluation)
4. Transition to next paragraph

## Literature Sources

### PubMed MCP (Biomedical Literature)

Access 35+ million biomedical literature citations.

**Configuration:**
```json
{
  "mcpServers": {
    "pubmedmcp": {
      "command": "uvx",
      "args": ["pubmedmcp@latest"],
      "env": {
        "UV_PRERELEASE": "allow",
        "UV_PYTHON": "3.12"
      }
    }
  }
}
```

**Search Strategy by Type:**

#### Type A (Paradigm/Ethics)
- Search for: "ethics", "cost-effectiveness", "patient attitudes", "position statements", "policy", "regulation", "societal impact", "equity"

#### Type B (Clinical Management)
- Search for: "guidelines", "screening sensitivity", "management protocols", "adherence", "barriers", "implementation", "clinical practice", "outcome measures"

#### Type C (Precision Medicine)
- Search for: "molecular pathway", "mouse models", "case reports", "genotype correlation", "mutation spectrum", "functional analysis", "targeted therapy"

**General Search Tips:**
- Use MeSH terms for precise genetic searches: "Genetics"[Mesh], "Rare Diseases"[Mesh]
- Combine with publication type filters (Review, Clinical Trial)
- Filter by date for recent literature
- Search terms: "gene*", "genetic*", "rare disease", "sequencing", "inherited disorder", "population genetics", "genome-wide association study"

### GeneCards (Genetic Database)

Access comprehensive human genes and genetic phenotypes database:
- URL: https://www.genecards.org/
- Search for gene-disease associations
- Extract functional annotations

### OMIM (Online Mendelian Inheritance in Man)

Database of human genes and genetic disorders:
- URL: https://omim.org/
- Access gene-phenotype relationships
- Retrieve inheritance patterns

### dbGaP (Database of Genotypes and Phenotypes)

Repository of genomic and phenotype data:
- URL: https://www.ncbi.nlm.nih.gov/gap
- Access GWAS studies and sequencing data
- Extract statistical results

### ClinVar (Clinical Variant Database)

Relationships between genetic variations and phenotypes:
- URL: https://www.ncbi.nlm.nih.gov/clinvar/
- Access clinical significance of variants
- Extract variant-disease associations

### Source Selection Guide

| Source | Best For | Strengths |
|--------|----------|-----------|
| **PubMed** | Comprehensive literature, peer-reviewed | Extensive coverage, MeSH indexing, clinical relevance |
| **GeneCards** | Gene-disease associations | Comprehensive annotations, expression data |
| **OMIM** | Rare disease genetics | Curated gene-phenotype relationships |
| **dbGaP** | Population genetics, GWAS | Large-scale genetic studies, statistical results |
| **ClinVar** | Clinical interpretation | Variant pathogenicity, clinical significance |

## Standard Review Structure by Type

### Type A Structure (Paradigm/Ethics Focus)
```markdown
# [Title]: [Topic] and [Policy/Ethics/Regulatory] Implications

## Key Points
- [3-5 bullets summarizing main findings and implications]

## Abstract

## 1. Introduction: The Conflict/New Technology
### 1.1 Technical Background
### 1.2 Current State of Practice

## 2. Estimated Benefits (Models vs. Data)
### 2.1 Theoretical Advantages
### 2.2 Evidence Base for Benefits

## 3. Harms & Limitations (Personal & Societal)
### 3.1 Individual Risks
### 3.2 Societal Concerns

## 4. Stakeholder Perspectives
### 4.1 Patient Views
### 4.2 Professional Opinions
### 4.3 Regulatory Considerations

## 5. Policy Recommendations
### 5.1 Framework Development
### 5.2 Implementation Strategies

## 6. Discussion
### 6.1 Ethical Considerations
### 6.2 Equity and Access
### 6.3 Cost-Benefit Analysis
### 6.4 Future Directions

## 7. Conclusion

## Figures and Tables
**Table 1. Benefit-Risk Analysis Matrix**
| Factor | Theoretical Benefit | Real-World Evidence | Risk Level |
|--------|-------------------|-------------------|------------|
|        |                   |                   |            |

**Figure 1. Stakeholder Perspective Web**
[Description of stakeholder relationship visualization]

## References
```

### Type B Structure (Clinical Management Focus)
```markdown
# [Title]: [Disease/Condition] Management and Clinical Implementation

## Key Points
- [3-5 bullets summarizing main findings and clinical recommendations]

## Abstract

## 1. Introduction: Disease Burden
### 1.1 Epidemiological Context
### 1.2 Clinical Significance

## 2. Identification & Risk Assessment
### 2.1 Screening Criteria
### 2.2 Risk Stratification

## 3. Surveillance Strategies (Imaging/Biomarkers)
### 3.1 Recommended Protocols
### 3.2 Monitoring Guidelines

## 4. Risk Reduction (Medical/Surgical)
### 4.1 Non-surgical Interventions
### 4.2 Surgical Options

## 5. Implementation Barriers (The "Real World")
### 5.1 Psychological Factors
### 5.2 Financial Constraints
### 5.3 Systemic Issues

## 6. Future: Personalized Prevention
### 6.1 Emerging Technologies
### 6.2 Tailored Approaches

## 7. Discussion
### 7.1 Clinical Practice Gaps
### 7.2 Implementation Challenges
### 7.3 Future Research Needs

## 8. Conclusion

## Figures and Tables
**Table 1. Clinical Management Recommendations by Risk Level**
| Risk Level | Surveillance | Intervention | Frequency |
|------------|--------------|--------------|-----------|
|            |              |              |           |

**Figure 1. Clinical Decision Algorithm**
[Flowchart showing clinical management pathway]

## References
```

### Type C Structure (Precision Medicine Focus)
```markdown
# [Title]: [Gene/Disease] Molecular Mechanisms and Targeted Approaches

## Key Points
- [3-5 bullets summarizing main findings and molecular insights]

## Abstract

## 1. Introduction: Clinical Phenotype
### 1.1 Disease Presentation
### 1.2 Clinical Challenges

## 2. Genetic Architecture (Mutational Spectrum)
### 2.1 Mutation Types
### 2.2 Genotype-Phenotype Correlations

## 3. Molecular Pathogenesis (The Pathway)
### 3.1 Pathway Disruption
### 3.2 Cellular Consequences

## 4. Genotype-Phenotype Correlations
### 4.1 Phenotypic Variability
### 4.2 Severity Predictors

## 5. Emerging Targeted Therapies
### 5.1 Mechanism-Based Treatments
### 5.2 Clinical Trial Results

## 6. Conclusion: From Bench to Bedside

## Figures and Tables
**Table 1. Gene Mutations and Associated Phenotypes**
| Mutation | Location | Effect | Phenotype | Severity |
|----------|----------|--------|-----------|----------|
|          |          |        |           |          |

**Figure 1. Molecular Signaling Pathway**
[Detailed mechanism diagram showing the disrupted pathway]

## References
```

## Phased Writing Approach

When writing the review, follow the appropriate phased approach based on the selected type:

### Phase 1: Strategic Alignment (Initialization)
- Analyze user topic against Type A/B/C definitions
- Confirm mode: "Based on your topic, I recommend **Type [X]** strategy because..."
- Generate `CLAUDE.md` with mode-specific guidelines

### Phase 2: Targeted Literature Mining
- Use mode-specific search strategies
- Focus on relevant databases and metrics
- Gather appropriate types of evidence

### Phase 3: Structural Blueprinting (Outline)
- Create `IMPLEMENTATION_PLAN.md` with mode-specific headers
- Use appropriate skeleton structure
- Plan for required tables and figures

### Phase 4: High-Density Drafting
- Write section by section using mode-appropriate tone and focus
- Integrate data with mode-specific metrics and analysis
- Maintain consistent style throughout

### Phase 5: Visual Synthesis (Figures & Tables)
- Create mandatory outputs based on mode:
  - Type A: "Benefit-Risk Balance Scale" or "Stakeholder Web"
  - Type B: "Clinical Decision Algorithm" (Flowchart)
  - Type C: "Molecular Signaling Pathway" (Mechanism Diagram)
- Generate core data tables appropriate to the mode

### Phase 6: Final Polish
- Ensure wider implications section aligns with target audience
- Verify citation format and completeness

## Method Description Template by Type

### Type A (Paradigm/Ethics)
```markdown
### [Section]: [Technology/Approach] Benefits vs. Harms

[1-2 paragraph introduction with context]

**[Approach Name]:** [Author] et al. [ref] developed [approach], which [innovation] with potential benefits of [benefits] and theoretical risks of [risks].

**Stakeholder Impact:** The approach affects [stakeholder 1], [stakeholder 2], and [stakeholder 3] by [effects].

**Ethical Considerations:** Despite advantages, [category] approaches raise: (1) [ethical concern 1]; (2) [ethical concern 2]; (3) [equity issue].
```

### Type B (Clinical Management)
```markdown
### [Section]: [Management Approach] Implementation

[1-2 paragraph introduction with motivation]

**[Management Protocol]:** [Author] et al. [ref] developed [protocol], which [approach] for [condition]:
- Recommended for [risk group]
- Performed every [frequency]
Shows [efficacy metrics] in [cohort].

**Implementation Barriers:** Despite effectiveness, [category] approaches face: (1) [barrier 1]; (2) [barrier 2]; (3) [access issue].
```

### Type C (Precision Medicine)
```markdown
### [Section]: [Molecular Mechanism/Therapy] Action

[1-2 paragraph introduction with motivation]

**[Mechanism/Therapy]:** [Author] et al. [ref] discovered [mechanism], which [process] through [pathway]:
- Affects [cellular component 1]
- Modulates [pathway element 2]
Causes [phenotypic outcome] in [cohort] with [genetic variant].

**Molecular Targeting:** The approach exploits [molecular feature] to [therapeutic goal], incorporating [key elements].
```

## Citation Patterns

```markdown
# Data citation
"...identified variants with OR of 2.34 [23]"

# Method citation
"Johnson et al. [45] developed..."

# Multi-citation
"Several studies identified... [12, 15, 23]"

# Comparative
"While [12] focused on..., [15] addressed..."
```

## Genetic Terminology Guidelines

### Nomenclature Standards
- Gene symbols: italicized (e.g., *BRCA1*)
- Protein products: not italicized (e.g., BRCA1 protein)
- Chromosome locations: chr1q21.1
- SNPs: rs12345678
- HGVS notation: c.123A>G (DNA), p.Lys41Arg (protein)

### Statistical Reporting (Type B)
- Odds ratios: OR = X.XX (95% CI: X.XX-X.XX, P<0.05)
- Effect sizes: Cohen's d = X.XX
- P-values: P<0.001, P=0.045 (not P<0.05)
- Allele frequencies: 0.XX (X%)

### Benefit/Risk Metrics (Type A)
- Cost-effectiveness ratios: ICER = $X,XXX per QALY
- Risk ratios: RR = X.XX (95% CI: X.XX-X.XX)
- Net health benefit: NHB = X.XX at willingness-to-pay of $X,XXX

### Molecular Metrics (Type C)
- Expression levels: fold-change X.XX (P<0.05)
- Binding affinity: Kd = X.XX μM
- Pathway activity: normalized to control = X.XX ± X.XX

## Quality Checklist

Before completion, verify:
- [ ] Correct review type (A/B/C) has been selected and applied
- [ ] Mode-specific Key Points present (3-5 bullets)
- [ ] Mode-specific Tables created per major section
- [ ] Appropriate limitations section for the review type
- [ ] Consistent terminology throughout
- [ ] Appropriate tone for the selected review type
- [ ] 30-80 references, organized by topic
- [ ] Mode-specific Figure placeholders with captions
- [ ] Proper genetic nomenclature
- [ ] Appropriate statistical reporting standards for the type
- [ ] Wider implications section addresses the correct audience

## File References

- [WORKFLOW.md](WORKFLOW.md) - Detailed phase-specific workflow
- [TEMPLATES.md](TEMPLATES.md) - CLAUDE.md and IMPLEMENTATION_PLAN.md templates
- [DOMAINS.md](DOMAINS.md) - Domain-specific method categories
- [GLOSSARY.md](GLOSSARY.md) - Genetic terminology reference