# HTAIS - Hallucination Taxonomy for AI Systems

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Version](https://img.shields.io/badge/version-1.2-blue.svg)](https://github.com/mosaicdm/htais/releases)

A comprehensive taxonomy for identifying and classifying AI hallucinations across 22 distinct types.

HTAIS provides a systematic framework for understanding, identifying, and classifying AI output failures. The goal is to have a well defined taxonomy of hallucination types and classes. If we can mitigate entire classes of hallucinations, or better, eliminate them completely, then we can step closer to AI Safety and safety of probabilistic systems.

---

## Table of Contents

- [What is HTAIS?](#what-is-htais)
- [The Taxonomy](#the-taxonomy)
- [Quick Start](#quick-start)
- [Application Domains](#application-domains)
- [Use Cases](#use-cases)
- [Citation](#citation)
- [Professional Services](#professional-services)
- [License](#license)

---

## What is HTAIS?

AI systems increasingly generate content that appears plausible but is factually incorrect, logically inconsistent, or misleading. These "hallucinations" represent a critical challenge for AI deployment, particularly in safety-critical, financial, and regulatory contexts.

**HTAIS addresses this by providing:**

* Comprehensive Classification: 22 distinct hallucination types across 5 categories
* Universal Framework: Applicable to any AI system with probabilistic outputs
* Clear Definitions: Unambiguous categorization with concrete examples
* Domain Coverage: Applicable across 10+ application areas
* Research Foundation: Enables systematic measurement and comparison

## Scope and Intent

HTAIS defines a **classification framework** for identifying and naming hallucination and failure modes in AI system outputs.

It is intentionally limited to:
- precise terminology
- observable failure definitions
- category boundaries

HTAIS does **not** specify:
- how hallucinations are detected
- how failures are scored or prioritized
- how enforcement or blocking decisions are made
- how correctness is operationalized in production systems

Those concerns are **implementation-specific** and depend on system architecture, execution guarantees, and risk tolerance.

### Why HTAIS Matters

- **For Researchers**: Systematic classification enables rigorous evaluation and benchmarking
- **For Awesome Devs (Engineers)**: Clear categories guide detection and prevention strategies
- **For Organizations**: Risk assessment and quality assurance frameworks
- **For Regulators**: Common language for AI safety requirements
- **For the Field**: Shared vocabulary accelerates progress on AI reliability

---

## The Taxonomy

HTAIS organizes 22 hallucination types into five primary categories:

### Category Overview

| Category | Types | Focus Area | Example |
|----------|-------|------------|---------|
| **Factual** | H1-H5 | Incorrect or unsupported claims | Fabricating sources, inventing statistics |
| **Contextual** | H6-H8 | Context interpretation failures | Out-of-scope assertions, context drift |
| **Temporal** | H9-H11 | Time-related errors | Outdated facts, anachronisms |
| **Logical** | H12-H14 | Reasoning failures | Self-contradictions, invalid inferences |
| **Operational** | H15-H22 | System behavior issues | Overconfidence, fake tool use |

### Complete Type List

**Factual Hallucinations (H1-H5)**

- **H1: Unsupported Factual Claim** - Assertions without adequate grounding
- **H2: Fabricated Source** - Citations to non-existent sources
- **H3: Fabricated Detail** - Incorrect specifics added to accurate information
- **H4: Fabricated Relationship** - False connections between entities
- **H5: False Pattern Detection** - Claiming patterns that don't exist

**Contextual Hallucinations (H6-H8)**

- **H6: Out-of-Scope Assertion** - Claims beyond defined boundaries
- **H7: Hidden Claim** - Unsupported assumptions embedded in responses
- **H8: Context Drift** - Gradual deviation from original context

**Temporal Hallucinations (H9-H11)**

- **H9: Outdated Fact** - Previously true information presented as current
- **H10: Premature Assertion** - Claiming events occurred before they happen
- **H11: Anachronism** - Placing concepts in incorrect temporal contexts

**Logical Hallucinations (H12-H14)**

- **H12: Self-Contradiction** - Mutually incompatible claims
- **H13: Incompatible Constraints** - Unsatisfiable requirement combinations
- **H14: Invalid Inference** - Conclusions that don't follow from premises

**Operational Hallucinations (H15-H22)**

- **H15: Overconfidence** - Inappropriate certainty about uncertain information
- **H16: Missing Qualification** - Failure to provide necessary context or limitations
- **H17: Authority Inflation** - Claiming capabilities beyond actual design
- **H18: Fake Tool Use** - Claiming tool execution without actually running it
- **H19: Imaginary Computation** - Presenting computational results without execution
- **H20: Broken Schema** - Violating specified formats or structures
- **H21: Silent Failure** - Proceeding despite errors without indication
- **H22: Type/Category Confusion** - Applying reasoning inappropriately across domains

---

## Quick Start

### View the Taxonomy

**Interactive HTML Table:**
- [htais-v1.2-public-taxonomy.html](htais-v1.2-public-taxonomy.html)
- [htais-v1.2-public-taxonomy.pdf](htais-v1.2-public-taxonomy.pdf)

### Explore the Visualization

**Interactive Topology Map:**
- [htais-topology-visualization-public.html](htais-topology-visualization-public.html)

Features:
- Color-coded regions by computational domain
- Click nodes to see detailed information
- Filter by application domain
- See prevalence indicators

### Learn Applications

**Read Domain Guide:**
- [htais-application-domains-public.md](htais-application-domains-public.md)

Covers:
- Large Language Models
- Generative AI (images, video, audio)
- Medical diagnosis systems
- Autonomous systems and robotics
- Financial modeling
- Code generation
- Scientific simulation
- And more...

---

## Application Domains

HTAIS applies to **any AI system with probabilistic outputs**, particularly when:

- Outputs are generated from learned patterns (not pure retrieval)
- Ground truth verification is expensive or delayed
- Errors have significant consequences (safety, financial, regulatory)
- In practice, HTAIS is most effective when paired with systems capable of enforcing correctness constraints on AI outputs.

### Applicable Domains

| Domain | Key Hallucination Types | Why It Matters |
|--------|------------------------|----------------|
| **LLMs** | H1, H2, H9, H15, H22 | User trust, information accuracy |
| **Generative AI** | H1, H4, H5, H22 | Professional use, brand reputation |
| **Medical Diagnosis** | H1, H5, H14, H15 | Patient safety, regulatory compliance |
| **Molecular Design** | H1, H12, H13, H22 | R&D efficiency, synthesis validity |
| **Autonomous Systems** | H1, H9, H10, H18, H22 | Physical safety, liability |
| **Financial Modeling** | H1, H5, H8, H15, H22 | Risk management, regulatory compliance |
| **Code Generation** | H1, H18, H19, H20, H22 | Software reliability, security |
| **Scientific Simulation** | H1, H12, H19, H22 | Research credibility, reproducibility |
| **Synthetic Data** | H3, H4, H5, H8 | Training quality, privacy preservation |
| **Translation** | H1, H3, H6, H8 | Communication accuracy, cultural fidelity |

See [htais-application-domains-public.md](htais-application-domains-public.md) for detailed coverage.

---

## Non-Goals

HTAIS is not intended to:
- replace model evaluation frameworks
- prescribe confidence scores or probabilities
- act as a runtime policy engine
- guarantee truth, accuracy, or safety on its own

HTAIS provides a shared paradigm and classification for failure analysis.
Correctness enforcement requires additional systems.

---

## Use Cases

### Research & Evaluation

**Benchmark Creation:**
- Systematically cover all 22 hallucination types
- Enable standardized comparison across models
- Measure hallucination rates by category

**Performance Measurement:**
- Track hallucination rates over time
- Compare across different architectures
- Measure by domain or use case

### Production Deployment

**Quality Assurance:**
- Classify outputs by HTAIS type
- Prioritize mitigation by severity
- Track rates in production
- Continuous improvement loops

**Risk Assessment:**
- Identify which hallucination types are most likely
- Understand consequences in your domain
- Develop detection and prevention strategies

### Team Communication

**Common Language:**
- Replace: "The AI made something up"
- With: "H2 violation - Fabricated Source"

**Precise Documentation:**
- "Our system is tested against all 22 HTAIS types"
- "Hallucination rate: H1 <2%, H15 <5%"
- "Mitigation strategies implemented for safety-critical types"

---

## Citation

If you use HTAIS in your research, products, or publications, please cite:

### BibTeX

```bibtex
@misc{acosta2026htais,
  author = {Acosta, Mark},
  title = {HTAIS: Hallucination Taxonomy for AI Systems},
  year = {2026},
  version = {1.2},
  publisher = {MosaicDM LLC},
  url = {https://github.com/mosaicdm/htais},
  license = {CC-BY-4.0}
}
```

### APA Style

> Acosta, M. (2026). *HTAIS: Hallucination Taxonomy for AI Systems* (Version 1.2). MosaicDM LLC. https://github.com/mosaicdm/htais

### MLA Style

> Acosta, Mark. "HTAIS: Hallucination Taxonomy for AI Systems." Version 1.2, MosaicDM LLC, 2026, github.com/mosaicdm/htais.

### Chicago Style

> Acosta, Mark. 2026. "HTAIS: Hallucination Taxonomy for AI Systems." Version 1.2. MosaicDM LLC. https://github.com/mosaicdm/htais.

---

## Professional Services

While HTAIS is freely available under **CC BY 4.0**, MosaicDM offers commercial-grade implementation and consulting for organizations requiring production-ready solutions.

### What We Provide

**Mathematical correctness enforcement frameworks**

**HTAIS-Certified Tools**

**Custom Integration**

**Safety-Critical Validation**

**Training & Consulting**

### Why Professional Implementation?

The open taxonomy enables **classification**. Our commercial tools provide **detection**:

| Open Taxonomy | Commercial Tools |
|---------------|------------------|
| Definitions and categories | Mathematical detection framework |
| Conceptual framework | Real-time implementation |
| Examples | Accuracy Correctness |
| Public documentation | Formal verification |
| Community standard | Production support |

### Contact

**Email:** contact@mosaicdm.co  
**Website:** https://mosaicdm.co

---

## License

**HTAIS v1.2** is licensed under [**Creative Commons Attribution 4.0 International (CC BY 4.0)**](https://creativecommons.org/licenses/by/4.0/).

### You are free to:

- **Share** - copy and redistribute the material in any medium or format
- **Adapt** - remix, transform, and build upon the material for any purpose, even commercially

### Under the following terms:

**Attribution** - You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.

### Proper Attribution

When using HTAIS, include:

```
This work uses HTAIS (Hallucination Taxonomy for AI Systems) v1.2 
by Mark Acosta, MosaicDM LLC, licensed under CC BY 4.0.
https://github.com/mosaicdm/htais
```

---

## FAQ

**Q: Is HTAIS only for LLMs?**

A: No. HTAIS applies to any AI system with probabilistic outputs - LLMs, generative AI, autonomous systems, medical AI, scientific simulation, code generation, and more. The taxonomy is universal.

**Q: How are HTAIS categories used in detection systems?**

A: The open taxonomy provides classification. Detection implementation requires technical expertise and domain-specific approaches. MosaicDM offers commercial tools with mathematical guarantees.

**Q: Can I use HTAIS in commercial products?**

A: Yes. CC BY 4.0 allows commercial use. Just provide proper attribution.

**Q: How is this different from other hallucination taxonomies?**

A: HTAIS is the first comprehensive( we could not find anything else, so we did this ourselves ) taxonomy covering 22 distinct types with universal applicability. It's applicable across 10+ domains and provides clear definitions with concrete examples.

**Q: Can I propose new hallucination types?**

A: Yes. Open an issue with clear definition, examples, and justification for why it's distinct from existing types.

**Q: Is there a paper?**

A: Academic publication is planned for 2026. Contact us about collaboration opportunities.

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| **1.2** | January 2026 | Public release with interactive visualization, application domains guide |
| **1.1** | January 2026 | Added H21 (Silent Failure) and H22 (Type Confusion), refined categories |
| **1.0** | January 2026 | Initial taxonomy with 20 types across 5 categories |

---

## About MosaicDM

**MosaicDM LLC** develops Dimensional Intelligence (DI) technology - mathematically rigorous frameworks that provide provably correct AI systems through geometric computation.

HTAIS represents our contribution to advancing AI safety and reliability across the industry. By providing this taxonomy as a community resource, we aim to accelerate progress on one of AI's most critical challenges.

### Our Mission

Build infrastructure for verified intelligence at scale - AI systems with mathematical guarantees of correctness, zero hallucination rates, and complete auditability.

### Learn More

**Website:** https://mosaicdm.co  
**Contact:** contact@mosaicdm.co

---

## Acknowledgments

Thank you to the AI safety, machine learning, and broader research communities whose work on AI reliability and interpretability informed this taxonomy.

---

<div align="center">

**Made with care by [MosaicDM](https://mosaicdm.co)**

**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) • **Version:** 1.2 • **Updated:** January 2026

</div>
