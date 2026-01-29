---
name: generate-genetic-review
description: Write comprehensive literature reviews for genetic research, rare diseases, and genomic sequencing. Use when writing survey papers, systematic reviews, or literature analyses on topics like gene therapy, rare genetic disorders, whole genome sequencing, inherited disorders, population genetics, and genomic medicine. Triggers on requests for "genetic review", "rare disease review", "gene therapy survey", "genomic medicine literature review", or mentions of writing academic reviews on genetics, genomics, or inherited disorders. References in 30-80 range. Word count 4000-8000 words. Integrates with Google NotebookLM to read provided PDFs and cite their references.
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

# Genetic Research Literature Review Writing Skill

A systematic workflow for writing comprehensive literature reviews in genetic research, rare diseases, and genomic medicine.

## Quick Start

When user requests a genetic literature review:

1. **Initialize project** with core files:
   - `CLAUDE.md` - Writing guidelines and terminology
   - `IMPLEMENTATION_PLAN.md` - Staged execution plan
   - `manuscript_draft.md` - Main manuscript
   - `REFERENCES_PDF.md` - Extracted references from provided PDFs
   - `DATA_SUMMARY.md` - Summary of key data points from PDFs

2. **Follow the phased writing workflow** (see [WORKFLOW.md](WORKFLOW.md)):
   - Title and Keypoints
   - Abstract
   - Introduction
   - Methods
   - Results (with tables and figures)
   - Discussion
   - Conclusion
   - Figures and Tables
   - References

3. **Integrate PDF sources** via Google NotebookLM (if provided)

## PDF Integration with Google NotebookLM

When user provides PDFs for reference:

1. **Upload to NotebookLM** for content extraction
2. **Extract key references** and integrate into review
3. **Summarize data** for inclusion in tables and figures
4. **Maintain citation integrity** throughout manuscript

### Configuration for NotebookLM Integration:
```json
{
  "notebooklm": {
    "enabled": true,
    "api_key_required": true,
    "supported_formats": ["pdf", "docx", "txt", "html"],
    "reference_extraction": true,
    "data_table_generation": true
  }
}
```

## Core Principles

### Writing Style
- Use **hedging language**: "may", "suggests", "appears to", "has shown promising results"
- Avoid absolute claims: Never say "X is the definitive genetic cause"
- Every claim needs citation support
- Each method section needs a **Limitations** paragraph

### Required Elements
- **Key Points box** (3-5 bullets) after title
- **Comparison table** for each major section
- **Genetic metrics** with consistent format (OR: X.XX, P-value: <0.05, Effect size: X.XX)
- **Figure placeholders** with detailed captions
- **References organized by topic** (30-80 typical)

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

**Search Tips:**
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

## Standard Review Structure

```markdown
# [Title]: Advances in [Genetic Topic] and Clinical Implications

## Key Points
- [3-5 bullets summarizing main findings]

## Abstract

## 1. Introduction
### 1.1 Genetic Background
### 1.2 Clinical Significance
### 1.3 Scope and Contributions

## 2. Methods
### 2.1 Literature Search Strategy
### 2.2 Inclusion/Exclusion Criteria
### 2.3 Data Extraction Process
### 2.4 Quality Assessment

## 3. Results
### 3.1 [Main Finding Category 1]
### 3.2 [Main Finding Category 2]
...
**Table 1. [Title of Key Data Summary Table]**
| Column 1 | Column 2 | Column 3 | Column 4 | Column 5 |
|----------|----------|----------|----------|----------|
| Data     | Data     | Data     | Data     | Data     |

**Table 2. [Title of Secondary Data Summary Table]**
| Column 1 | Column 2 | Column 3 | Column 4 |
|----------|----------|----------|----------|
| Data     | Data     | Data     | Data     |

**Figure 1. [Caption for Main Figure]**
Description of the visual content that would appear in this figure, including key data trends or relationships.

**Figure 2. [Caption for Secondary Figure]**
Description of the visual content that would appear in this figure, including comparative data or mechanistic pathways.

## 4. Genetic Technologies and Datasets
### 4.1 Sequencing Technologies
### 4.2 Population Databases

## 5. Genetic Disorders and Mechanisms
### 5.1 [Disorder Category 1]
### 5.2 [Disorder Category 2]
...

## 6. Clinical Applications
### 6.1 Diagnostic Applications
### 6.2 Therapeutic Applications
### 6.3 Population Screening

## 7. Discussion
### 7.1 Interpretation of Findings
### 7.2 Clinical Implications
### 7.3 Limitations
### 7.4 Future Directions

## 8. Conclusion

## Figures and Tables
[Detailed descriptions of all figures and tables with data sources]

## References
```

## Phased Writing Approach

When writing the review, follow this sequential approach:

### Phase 1: Title and Keypoints
- Create an informative title reflecting the scope
- Write 3-5 key points summarizing main findings

### Phase 2: Abstract
- Write structured abstract (background, methods, results, conclusions)

### Phase 3: Introduction
- Establish genetic background and clinical significance
- Define scope and contributions

### Phase 4: Methods
- Detail literature search strategy
- Specify inclusion/exclusion criteria
- Describe data extraction process

### Phase 5: Results
- Present main findings with data summary tables
- Include figure descriptions with detailed captions
- Reference data from provided PDFs where applicable

### Phase 6: Discussion
- Interpret findings in clinical context
- Address limitations
- Propose future directions

### Phase 7: Conclusion
- Summarize key findings and implications

### Phase 8: Figures and Tables
- Provide detailed descriptions of all visual elements
- Include data sources and statistical information

### Phase 9: References
- Compile all sources in proper format
- Include references from both literature search and provided PDFs

## Method Description Template

```markdown
### 4.X [Method Category]

[1-2 paragraph introduction with motivation]

**[Method Name]:** [Author] et al. [ref] developed [method], which [innovation]:
- [Key component 1]
- [Key component 2]
Identified variants with OR of X.XX (P<0.05) in [cohort].

**Algorithmic Approach:** (if applicable)
The method uses [approach] to [goal], incorporating [key elements].

**Limitations:** Despite advantages, [category] methods face: (1) [limit 1]; (2) [limit 2].
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

### Statistical Reporting
- Odds ratios: OR = X.XX (95% CI: X.XX-X.XX, P<0.05)
- Effect sizes: Cohen's d = X.XX
- P-values: P<0.001, P=0.045 (not P<0.05)
- Allele frequencies: 0.XX (X%)

## Quality Checklist

Before completion, verify:
- [ ] Key Points present (3-5 bullets)
- [ ] Table per major section
- [ ] Limitations for each method category
- [ ] Consistent terminology throughout
- [ ] Hedging language used appropriately
- [ ] 30-80 references, organized by topic
- [ ] Figure placeholders with captions
- [ ] Proper genetic nomenclature
- [ ] Statistical reporting standards met

## File References

- [WORKFLOW.md](WORKFLOW.md) - Detailed 7-phase workflow
- [TEMPLATES.md](TEMPLATES.md) - CLAUDE.md and IMPLEMENTATION_PLAN.md templates
- [DOMAINS.md](DOMAINS.md) - Domain-specific method categories
- [GLOSSARY.md](GLOSSARY.md) - Genetic terminology reference