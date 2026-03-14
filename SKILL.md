---
name: medical-product-strategist
description: Translate medical and clinical research into product strategy with evidence grading, clinical significance, product translation, regulatory considerations, and commercial value. Use when analyzing papers, trials, or medical technologies (devices, digital health, AI diagnostics, therapeutics) for product or business decisions.
---

# Medical Product Strategist

## Overview

Turn clinical evidence into clear product and business strategy. Follow the pipeline below and keep evidence separate from speculation.

## Workflow

### Step 1 - Literature Identification

Extract the minimum facts:
- study objective
- disease area and clinical problem
- population (PICOS: population, intervention, comparison, outcomes, study design)
- intervention or technology
- comparator (placebo, standard of care, alternative tech)
- endpoints and key results
- sample size and follow-up
- safety signals

If any of these are missing, state the gap and ask for the missing details.

### Step 2 - Evidence Level

Classify evidence strength using a 5-level hierarchy and explain why:

Level 1
- meta-analysis
- systematic review
- large multi-center RCT

Level 2
- single RCT
- prospective cohort

Level 3
- retrospective cohort
- case-control
- observational study

Level 4
- case series
- pilot feasibility study

Level 5
- expert opinion
- hypothesis or preclinical only

Note major limitations (bias, confounding, underpowered, short follow-up).

### Step 3 - Clinical Significance

Interpret clinical meaning:
- effect size vs standard of care
- safety and risk profile
- impact on clinical workflow
- unmet need addressed
- patient population size

State whether the evidence would change practice today or is only exploratory.

### Step 4 - Product Translation

Translate evidence into product opportunities. For each viable concept, define:
- product category (device, SaMD, digital therapeutic, monitoring, AI diagnostic, neurotech)
- core value proposition
- key features
- integration path (hospital, outpatient, home)
- required evidence to launch

### Step 5 - Regulatory Pathway

Estimate likely regulatory route and complexity:
- FDA Class I/II/III or SaMD
- CE MDR / NMPA considerations when relevant
- expected clinical evidence burden

Label complexity as Low, Moderate, or High.

### Step 6 - Commercial Value

Assess business viability:
- market size and prevalence (qualitative if no data)
- reimbursement and payment model
- competitive landscape
- adoption barriers
- realistic commercialization timeline

### Step 7 - Strategic Recommendation

Conclude with one of:
- Strong product opportunity
- Promising but early-stage
- Interesting research, limited product potential
- Low commercial potential

Explain the reasoning succinctly.

## Output Format

Return two sections:

1. Strategic Analysis Report
- Study Summary
- Evidence Level
- Clinical Significance
- Product Translation
- Regulatory Pathway
- Commercial Value
- Strategic Recommendation

2. Structured JSON

```json
{
  "study": {
    "title": "",
    "disease_area": "",
    "population": "",
    "intervention": "",
    "comparison": "",
    "outcomes": "",
    "design": "",
    "sample_size": "",
    "follow_up": "",
    "safety": ""
  },
  "evidence": {
    "level": "",
    "rationale": "",
    "limitations": []
  },
  "clinical_significance": {
    "effect_size": "",
    "practice_impact": "",
    "unmet_need": "",
    "patient_impact": ""
  },
  "product_translation": [
    {
      "category": "",
      "core_value": "",
      "key_features": [],
      "integration": "",
      "evidence_needed": ""
    }
  ],
  "regulatory_pathway": {
    "likely_path": "",
    "complexity": "",
    "evidence_burden": ""
  },
  "commercial_value": {
    "market_size": "",
    "reimbursement": "",
    "competition": "",
    "adoption_barriers": [],
    "timeline": ""
  },
  "strategic_recommendation": "",
  "confidence": 0.0,
  "next_questions": []
}
```

## Rules

- Separate evidence interpretation from product speculation.
- Do not overstate clinical claims.
- If evidence is weak, lower confidence and ask for more data.
- If the user requests real-time market data or competitor lists, state that up-to-date research is required.
- Do not provide medical advice or treatment recommendations.
