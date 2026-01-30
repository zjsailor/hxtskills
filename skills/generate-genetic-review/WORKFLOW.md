# Adaptive Phased Execution Workflow for Genetic Literature Reviews

## Phase 1: Strategic Alignment (Initialization)
**Goal**: Classify the review type and define scope based on research purpose.

**Actions**:
1. **Analyze Input**: Assess user topic against Type A/B/C definitions
2. **Confirm Mode**: Explicitly state: "Based on your topic, I recommend **Type [X]** strategy because..."
3. **Generate `CLAUDE.md`**: Initialize project with mode-specific guidelines
4. **Define Scope**: Establish specific objectives aligned with selected type

**Deliverables**:
- Selected review type (A/B/C)
- Project-specific CLAUDE.md
- Defined scope and objectives

## Phase 2: Targeted Literature Mining
**Strategy varies by Mode**:

### Type A (Decision/Ethics) Mining:
- Search for: "ethics", "cost-effectiveness", "patient attitudes", "position statements", "policy", "regulation"
- Focus on societal impact studies
- Collect stakeholder opinion surveys
- Gather regulatory framework documents

### Type B (Clinical Management) Mining:
- Search for: "guidelines", "screening sensitivity", "management protocols", "adherence", "barriers", "implementation"
- Focus on clinical trials and cohort studies
- Collect outcome measurement data
- Gather implementation studies

### Type C (Mechanism/Precision) Mining:
- Search for: "molecular pathway", "mouse models", "case reports", "genotype correlation", "mutation spectrum", "functional analysis"
- Focus on mechanistic studies
- Collect case series and individual patient data
- Gather functional annotation studies

**Actions**:
1. Execute mode-specific search strategy
2. Apply inclusion/exclusion criteria
3. Extract relevant references and data points
4. Organize references by mode-appropriate categories

## Phase 3: Structural Blueprinting (Outline Creation)
Create `IMPLEMENTATION_PLAN.md` with mode-specific headers:

### Type A Skeleton
- Introduction: The Conflict/New Technology
- Technical Background
- Estimated Benefits (Models vs. Data)
- Harms & Limitations (Personal & Societal)
- Stakeholder Perspectives
- Policy Recommendations
- Discussion (Ethics, Equity, Cost-Benefit)

### Type B Skeleton
- Introduction: Disease Burden
- Identification & Risk Assessment
- Surveillance Strategies (Imaging/Biomarkers)
- Risk Reduction (Medical/Surgical)
- Implementation Barriers (The "Real World")
- Future: Personalized Prevention
- Discussion (Practice Gaps, Implementation Challenges)

### Type C Skeleton
- Introduction: Clinical Phenotype
- Genetic Architecture (Mutational Spectrum)
- Molecular Pathogenesis (The Pathway)
- Genotype-Phenotype Correlations
- Emerging Targeted Therapies
- Discussion (From Bench to Bedside)
- Conclusion

## Phase 4: High-Density Drafting
**Universal Rules**:
1. **Drafting**: Write section by section using mode-relevant approach
2. **Data Integration**:
    - *Type A*: Focus on benefit-risk statistics, stakeholder surveys, policy analyses
    - *Type B*: Focus on clinical outcomes, guideline recommendations, barrier assessments
    - *Type C*: Focus on molecular mechanisms, genotype correlations, case-level data

**Quality Requirements**:
- Every section begins with Key Points box (3-5 bullets)
- Each major section includes appropriate comparison table
- All claims supported by mode-appropriate evidence
- Proper hedging language maintained

## Phase 5: Visual Synthesis (Figures & Tables)
**Mandatory Outputs by Type**:

### Type A Required Visuals:
- **Figure 1 (Concept Map)**: "Benefit-Risk Balance Scale" or "Stakeholder Web"
- **Table 1 (Core Data)**: "Comparison of Model Predictions vs. Outcomes" or "Stakeholder Attitude Matrix"

### Type B Required Visuals:
- **Figure 1 (Concept Map)**: "Clinical Decision Algorithm" (Flowchart)
- **Table 1 (Core Data)**: "Screening/Intervention Recommendations by Risk Level"

### Type C Required Visuals:
- **Figure 1 (Concept Map)**: "Molecular Signaling Pathway" (Mechanism Diagram)
- **Table 1 (Core Data)**: "Summary of Gene Mutations and Associated Phenotypes"

## Phase 6: Final Polish
1. **Check "Wider Implications"**: Ensure the conclusion offers actionable advice for the specific target audience (Policymakers for Type A, Clinicians for Type B, Scientists for Type C).
2. **Reference Audit**: Verify `[n, Author, Year]` format and appropriate distribution by topic.
3. **Type Consistency**: Verify that the tone, focus, and content align with the selected review type.
4. **Quality Assurance**: Run through complete checklist before delivery.