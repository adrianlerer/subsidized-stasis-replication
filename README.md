# Subsidized Stasis: Replication Materials

**Paper:** "Subsidized Stasis: Fiscal Transfers as Exapted Selection Mechanism in Argentine Subnational Democracy"

**Author:** Ignacio Adrián Lerer

**SSRN:** [forthcoming]

**Date:** March 2026

---

## Repository Structure

```
├── paper/
│   └── paper_draft.md          # Full paper text (Markdown)
├── code/
│   └── fiscal_federalism_sim.py # Complete simulation: FSPI, CLI, EGT, PE analysis
├── data/
│   ├── perplexity_data_p6.md   # Reform chronology (9 attempts, 30 years)
│   ├── perplexity_data_p7.md   # Quantitative coparticipación data (IERAL, IARAF)
│   ├── perplexity_data_p9.md   # CSJN jurisprudence (hidden transcript)
│   └── perplexity_data_p10.md  # Comparative PE benchmarks (USA, India, Brazil)
├── figures/
│   ├── fspi_correlation.png    # H1: FSPI vs democratic quality (r=0.96)
│   ├── provincial_competition.png  # EGT simulation: transfers vs competitive
│   ├── ieral_ratio_democracy.png   # IERAL distortion vs democratic quality
│   └── employment_democracy.png    # Public employment vs democratic quality
└── swarm_analysis.md           # Cross-analysis with companion papers
```

## How to Replicate

### Requirements
```bash
pip install numpy scipy matplotlib
```

### Run the simulation
```bash
cd code/
python3 fiscal_federalism_sim.py
```

This produces:
- H1: FSPI-democracy correlation (r = 0.96, p < 0.0001)
- H2: CLI_copart = 0.997 with full reform chronology
- H3: Punctuation probability + scenario analysis
- IERAL ratio analysis
- Public employment as clientelism proxy
- Comparative PE benchmarks (USA/India/Brazil/Argentina)
- 4 figures saved to working directory

### Data Sources

| Data | Source | Year |
|------|--------|------|
| FSPI values | DNAP, Min. Economía, AFIP | 2024 |
| IERAL ratios | IERAL/Fundación Mediterránea | 2024 |
| Coparticipación coefficients | Ley 23.548, art. 4 | 1988 |
| Public employment | DNAP, INDEC-EPH, SIPA | 2024 |
| Democratic quality | Composite (Gervasoni SDI framework) | 2023 |
| Reform attempts | BCN, Infoleg, CSJN fallos | 1992-2025 |
| International comparison | IARAF, FMI, GST Council, Brazil Ministry | 2024 |

## Key Findings

| Hypothesis | Result | Evidence |
|------------|--------|----------|
| H1: FSPI → Democracy | r = 0.96 (p < 0.0001) | 24 provinces, all correlations significant |
| H2: CLI coparticipación | 0.997 (highest ever) | 9 attempts, 0 success, 30 years |
| H3: Punctuation threshold | shock ≥ 0.689 | Only hyperinflation breaks stasis |

## Companion Papers

This paper is part of a trilogy:

1. **Lerer (2025a):** "Argentina's Fiscal Lock-in: Tax Reform as Extended Phenotype" — SSRN 5635152
   - *Diagnosis:* Why reform is impossible (ESE, CLI_14bis = 0.89, Fiscal Trilemma)

2. **Lerer (2026):** "Subsidized Stasis" (this paper)
   - *Cost:* What the impossibility costs (FSPI, democratic degradation, exaptation)

3. **Lerer (2025b):** "Climbing Mount Improbable" — SSRN 5645070
   - *Prescription:* How to escape (gradual scaffolding, USD 15B guarantee fund)

## License

MIT License. Data and code freely available for replication and extension.

## Citation

```bibtex
@article{lerer2026subsidized,
  title={Subsidized Stasis: Fiscal Transfers as Exapted Selection Mechanism
         in Argentine Subnational Democracy},
  author={Lerer, Ignacio Adrián},
  year={2026},
  journal={SSRN Working Paper},
  url={https://github.com/adrianlerer/subsidized-stasis-replication}
}
```
