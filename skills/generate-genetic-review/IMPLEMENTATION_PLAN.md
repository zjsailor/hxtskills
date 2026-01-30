# Implementation Plan for Adaptive Genetic Literature Review

## Phase 1: Strategic Alignment (Review Type Selection)
- [ ] Analyze user topic against Type A/B/C definitions
- [ ] Confirm mode: "Based on your topic, I recommend **Type [X]** strategy because..."
- [ ] Generate project-specific CLAUDE.md with mode-specific guidelines
- [ ] Define specific genetic topic and scope appropriate to selected type
- [ ] Set reference limit (30-80 references)
- [ ] Establish word count target (4000-8000 words)
- [ ] Create project directory structure
- [ ] Initialize manuscript draft file
- [ ] Create REFERENCES_PDF.md for PDF references
- [ ] Create DATA_SUMMARY.md for key data points
- [ ] Collect and organize provided PDFs

## Phase 2: Targeted Literature Mining
### Type A (Decision/Ethics) Mining:
- [ ] Search for: "ethics", "cost-effectiveness", "patient attitudes", "position statements", "policy", "regulation"
- [ ] Focus on societal impact studies
- [ ] Collect stakeholder opinion surveys
- [ ] Gather regulatory framework documents

### Type B (Clinical Management) Mining:
- [ ] Search for: "guidelines", "screening sensitivity", "management protocols", "adherence", "barriers", "implementation"
- [ ] Focus on clinical trials and cohort studies
- [ ] Collect outcome measurement data
- [ ] Gather implementation studies

### Type C (Mechanism/Precision) Mining:
- [ ] Search for: "molecular pathway", "mouse models", "case reports", "genotype correlation", "mutation spectrum", "functional analysis"
- [ ] Focus on mechanistic studies
- [ ] Collect case series and individual patient data
- [ ] Gather functional annotation studies

### General Tasks:
- [ ] Execute mode-specific search strategy
- [ ] Apply inclusion/exclusion criteria relevant to selected type
- [ ] Document search strategy for reproducibility
- [ ] Prepare collected PDFs for NotebookLM upload

## Phase 3: PDF Processing with Google NotebookLM
- [ ] Upload PDFs to Google NotebookLM
- [ ] Extract key references from PDFs
- [ ] Identify important data points and statistics appropriate to selected type
- [ ] Summarize key findings from PDFs
- [ ] Add PDF references to REFERENCES_PDF.md
- [ ] Extract data points to DATA_SUMMARY.md
- [ ] Plan integration of PDF content into manuscript with type-appropriate focus

## Phase 4: Source Identification and Screening
- [ ] Execute literature search based on selected type
- [ ] Export results to reference manager
- [ ] Screen titles for relevance to selected type
- [ ] Assess abstracts against type-appropriate inclusion criteria
- [ ] Resolve conflicts in selection
- [ ] Document excluded articles and reasons
- [ ] Merge database results with PDF references

## Phase 5: Data Extraction and Organization
- [ ] Extract key information from selected articles
- [ ] Organize by type-appropriate categories (stakeholders for Type A, clinical pathways for Type B, mechanisms for Type C)
- [ ] Record type-appropriate statistical measures:
  - [ ] Type A: Cost-effectiveness ratios, risk ratios
  - [ ] Type B: Odds ratios, clinical outcomes
  - [ ] Type C: Expression levels, binding affinities
- [ ] Note study design and sample characteristics
- [ ] Identify key findings and limitations
- [ ] Create reference database
- [ ] Integrate data from DATA_SUMMARY.md
- [ ] Organize data for type-appropriate table creation

## Phase 6: Structural Blueprinting (Outline Creation)
### Type A Structure:
- [ ] Introduction: The Conflict/New Technology
- [ ] Technical Background
- [ ] Estimated Benefits (Models vs. Data)
- [ ] Harms & Limitations (Personal & Societal)
- [ ] Stakeholder Perspectives
- [ ] Policy Recommendations
- [ ] Discussion (Ethics, Equity, Cost-Benefit)

### Type B Structure:
- [ ] Introduction: Disease Burden
- [ ] Identification & Risk Assessment
- [ ] Surveillance Strategies (Imaging/Biomarkers)
- [ ] Risk Reduction (Medical/Surgical)
- [ ] Implementation Barriers (The "Real World")
- [ ] Future: Personalized Prevention
- [ ] Discussion (Practice Gaps, Implementation Challenges)

### Type C Structure:
- [ ] Introduction: Clinical Phenotype
- [ ] Genetic Architecture (Mutational Spectrum)
- [ ] Molecular Pathogenesis (The Pathway)
- [ ] Genotype-Phenotype Correlations
- [ ] Emerging Targeted Therapies
- [ ] Discussion (From Bench to Bedside)

### General Tasks:
- [ ] Develop hierarchical outline based on selected type
- [ ] Allocate approximate word counts per section
- [ ] Design type-appropriate Table 1
- [ ] Design type-appropriate Table 2
- [ ] Plan type-appropriate Figure 1
- [ ] Plan type-appropriate Figure 2
- [ ] Ensure balanced coverage appropriate to selected type

## Phase 7: Sequential Manuscript Composition
### Step 1: Title and Keypoints
- [ ] Write informative title reflecting selected type
- [ ] Create 3-5 key points summary for each major section

### Step 2: Abstract
- [ ] Write structured abstract (background, methods, results, conclusions) with type-appropriate focus

### Step 3: Introduction
- [ ] Establish background appropriate to selected type
- [ ] Define significance from type-appropriate perspective
- [ ] Outline scope and contributions

### Step 4: Methods
- [ ] Detail literature search strategy by type
- [ ] Specify type-appropriate inclusion/exclusion criteria
- [ ] Describe data extraction process
- [ ] Document quality assessment procedures

### Step 5: Results
- [ ] Present main findings with type-appropriate focus
- [ ] Create Table 1: Type-appropriate data summary with data from PDFs
- [ ] Create Table 2: Type-appropriate secondary data summary with data from PDFs
- [ ] Create Figure 1: Type-appropriate main data visualization description
- [ ] Create Figure 2: Type-appropriate secondary data visualization description

### Step 6: Content Sections
- [ ] Write remaining content sections with type-appropriate focus
- [ ] Integrate findings from provided PDFs
- [ ] Ensure proper citation of PDF sources
- [ ] Maintain tone appropriate to selected type

### Step 7: Discussion
- [ ] Interpret findings in type-appropriate context
- [ ] Address type-specific implications
- [ ] Address limitations
- [ ] Propose future directions

### Step 8: Conclusion
- [ ] Summarize key findings
- [ ] Highlight type-specific implications

### Step 9: Figures and Tables
- [ ] Provide detailed descriptions of all visual elements appropriate to type
- [ ] Include data sources and statistical information

### Step 10: References
- [ ] Compile all sources in proper format
- [ ] Include references from both databases and PDFs
- [ ] Ensure all citations are properly formatted

## Phase 8: Visual Synthesis (Figures & Tables)
### Type A Required Visuals:
- [ ] Figure 1: "Benefit-Risk Balance Scale" or "Stakeholder Web"
- [ ] Table 1: "Comparison of Model Predictions vs. Outcomes" or "Stakeholder Attitude Matrix"

### Type B Required Visuals:
- [ ] Figure 1: "Clinical Decision Algorithm" (Flowchart)
- [ ] Table 1: "Screening/Intervention Recommendations by Risk Level"

### Type C Required Visuals:
- [ ] Figure 1: "Molecular Signaling Pathway" (Mechanism Diagram)
- [ ] Table 1: "Summary of Gene Mutations and Associated Phenotypes"

## Phase 9: Final Polish
- [ ] Verify all claims have citation support
- [ ] Check adherence to genetic nomenclature standards
- [ ] Ensure statistical reporting is accurate and type-appropriate
- [ ] Confirm Key Points boxes are informative in each major section
- [ ] Review for type-appropriate tone and focus
- [ ] Validate reference count (30-80 range)
- [ ] Verify all PDF-derived data is properly cited
- [ ] Check "Wider Implications" section aligns with target audience:
  - [ ] Policymakers for Type A
  - [ ] Clinicians for Type B
  - [ ] Scientists for Type C
- [ ] Final proofread and formatting check

## Success Metrics
- [ ] Correct review type (A/B/C) selected and applied
- [ ] Manuscript addresses genetic topic with type-appropriate focus
- [ ] Reference count falls within 30-80 range
- [ ] Word count falls within 4000-8000 range
- [ ] Contains type-appropriate well-designed data summary tables
- [ ] Includes type-appropriate figures with detailed captions
- [ ] Successfully integrates provided PDF references
- [ ] All PDF-derived content is properly cited
- [ ] Each major section has Key Points box (3-5 bullets)
- [ ] Type-specific implications are clearly discussed
- [ ] Future directions are proposed with type-appropriate focus
- [ ] Writing follows type-appropriate guidelines
- [ ] Manuscript maintains consistency with selected review type