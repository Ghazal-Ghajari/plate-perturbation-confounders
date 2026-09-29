# Paper plan: figures, source notebooks, and coverage of the Aim 1 report

Working title: *Technical confounders of inter-individual variation and model evaluation in plate-based single-cell perturbation screens*
Target: Genome Biology (Research article). Authors: Ghazal Ghajari (all analyses, software, writing); Fathi Amsaad and T. K. Prasad (supervision, review) — confirm.

## 1. Main figures: panels, source notebook, result files

| Fig | Panel | Content | Notebook | Result files (already saved) | Plot status |
|---|---|---|---|---|---|
| 1 | a | Plate layouts of Parse and OP3 (schematic) | dictionary_position_check (1a), op3_benchmark_audit (1) | results/dictionary_position/cytokine_wells.csv; results/op3_benchmark_audit/compound_positions.csv | new plot |
| 1 | b | Inert cytokine "response" size vs. PBS | aim1_compass_parse (3b) | results/aim1/ | new plot |
| 1 | c | Alignment of inert responses with the shared axis | aim1_compass_parse (3b) | results/aim1/ | new plot |
| 1 | d | Responsive cytokines per cell type, PBS vs. inert reference | aim1_compass_parse (3c) | results/aim1/ | new plot |
| 2 | a | Within- vs. between-well differences, Parse (PBS) and OP3 (DMSO) | aim1_compass_parse (6c), op3_analysis (2) | results/op3_audit/dmso_well_noise*.csv | new plot |
| 2 | b | Cross-cell-type correlation of DMSO–DMSO pseudo-responses | op3_analysis (3) | results/op3_audit/dmso_shared_well_coordination.csv | new plot |
| 3 | a | Size/shape identity (schematic) | — | — | schematic |
| 3 | b | Asymmetric vs. symmetric estimator on Parse | aim1_compass_parse (12) | results/aim1/asymmetric_vs_symmetric_per_donor | new plot |
| 3 | c | Baseline IFN score by processing date/batch | aim1_replication_scbloodnl, aim1_replication_randolph_analysis (2) | results/aim1_replication/ifn_score_by_date.csv; results/aim1_replication3/randolph_donor_ifn.csv, randolph_ifn_score.png | exists / restyle |
| 3 | d | Simulations: false positives and power, naive vs corrected | aim1_simulation | results/aim1_simulation/simulation_summary.csv, .png | exists / restyle |
| 4 | a | Zahid audit: immune vs inert vs PBS-well pseudo-response | aim1_zahid_audit (5–7) | results/aim1_zahid_audit/coordination_by_reference.png, coordination_vs_strength.png | exists / restyle |
| 4 | b | Zahid audit across 4 spaces | aim1_zahid_audit (8) | coordination_by_space_summary.csv | new plot |
| 4 | c | OP3 row contamination | op3_benchmark_audit (3) | results/op3_benchmark_audit/row_contamination*.csv | new plot |
| 4 | d | DEG counts immune vs inert (DESeq2); reproducibility vs plate distance | dictionary_position_check (1b, 1c, 2) | results/dictionary_position/*.csv | new plot |
| 5 | a | Ceiling: same-well vs different-well correlation (inert) | aim1_benchmark_audit (3) | results/aim1_benchmark_audit/ceiling_same_vs_different_well.csv | new plot |
| 5 | b | Rhaister, additive, cytokine-free predictors: PBS vs re-referenced | rhaister_rescoring | results/rhaister_rescoring/scores_summary.csv | new plot |
| 5 | c | State vs baselines per split | state_rescoring (3) | results/state_rescoring/scores_summary.csv | new plot |
| 5 | d | Per-donor paired differences State – additive | state_rescoring (4) | results/state_rescoring/paired_state_vs_additive.csv, scores_per_context.csv | new plot |
| 6 | a | IFN shape effect in Parse (naive and corrected) | aim1_compass_parse (11, 13), donorvar_parse_example | results/aim1/corrected_pairs; results/donorvar_parse/by_pair.csv | new plot |
| 6 | b | Replication cohorts (1M-scBloodNL, Kang, Randolph) | three replication notebooks | results/aim1_replication*/ | new plot |
| 6 | c | donorvar workflow + Box 1 | — | — | schematic |

## 2. Supplementary figures / tables

| Supp | Content | Notebook |
|---|---|---|
| S1 | Receptor expression of inert proteins; full vs strict set | inert_receptor_check |
| S2 | COMPASS decomposition on Parse: between/within similarity, LODO transfer, component gains (Controls 1–2), SVD-1/SVD-3 robustness, family holdout, donor curve | aim1_compass_parse (4–10) |
| S3 | Pipeline validation on Replogle/Nadig (COMPASS reproduction) | aim0_compass_reproduction |
| S4 | Benchmark audit on Parse split: half-sample, additive, context mean, inert shift, both references | aim1_benchmark_audit |
| S5 | OP3 position effects (columns, edge rows) | op3_analysis (4) |
| S6 | Zahid audit: per-cytokine lollipop (PBS and inert references); strength vs excess | aim1_zahid_audit |
| S7 | Strict inert set: all audits repeated | zahid, rhaister, state, dictionary notebooks (INERT = strict) |
| S8 | Replication details: 1M-scBloodNL (date check, asymmetric vs corrected), Kang, Randolph (within batch, within ancestry) | replication notebooks |
| S9 | donorvar validation on Parse (per-cytokine vs pooled normalization) | donorvar_parse_example |
| T1 | Evidence table per technical source and dataset | report Table "tech" |
| T2 | Simulation settings and results | aim1_simulation |

## 3. Coverage check: every section of the Aim 1 report → manuscript

| Report section | Manuscript location |
|---|---|
| Why this aim / decomposition question | Background (para 1); case study; Fig. S2 |
| Dataset description | Results "Design of the screens"; Methods "Datasets" |
| Pipeline validation (Aim 0) | Results "Design"; Fig. S3 |
| Problems 1–5 (coverage, PBS shift, R² metric, noisy own-donor estimates, well noise) | Methods; Results "control wells", "well noise"; Fig. S2 |
| Responsive cytokines table | Results "control wells"; Fig. 1d |
| Between/within donor similarity; LODO transfer; component gains; Control 1 & 2 | Case study (last sentences); Fig. S2 |
| IFN group transfer table | Case study; Fig. 6a |
| Family holdout; donor curve | Fig. S2 (supplement text) |
| Robustness to decomposition (SVD-1, SVD-3) | Case study; Fig. S2 |
| Decomposition-free size/shape test | Results "estimator"; case study; Fig. 3a, 6a |
| Replication: 1M-scBloodNL, Kang, Randolph | Case study; Fig. 6b; Fig. S8 |
| Technical sources table | Table T1 |
| Asymmetric estimator on Parse | Results "estimator"; Fig. 3b |
| Simulations | Results "estimator"; Fig. 3d; Table T2 |
| Parse corrected pipeline table | Case study; Fig. 6a |
| Audit 1 (Zahid) + robustness to space | Results Audit 1; Fig. 4a,b; Fig. S6 |
| OP3 dataset (well noise, coordination, position) | Results "well noise"; Fig. 2; Fig. S5 |
| Audit 2 (OP3 targets) | Results Audit 2; Fig. 4c |
| Audit 3 (benchmarks, Rhaister, State) | Results Audit 3; Fig. 5; Fig. S4 |
| Audit 4 (DEG counts, position check) | Results Audit 4; Fig. 4d |
| Robustness to inert controls | Results "control wells" (receptor check); Fig. S1, S7 |
| Software (donorvar) | Conclusions; Code availability; Fig. 6c; Fig. S9 |
| Aquino request | Data availability (requested, not used) |
| What we could not answer | Discussion (limitations) |

## 4. Corrections found while preparing the paper
- The decomposition papers were conflated in the report ("COMPASS; Molina & Zhang"). COMPASS is Liang & Singh (bioRxiv 2026, 10.64898/2026.08.03.742643); the related decomposition preprint is Molina & Zhang (bioRxiv 2026, 10.64898/2026.07.24.740459). Aim 0 reproduces COMPASS.
- State is now published: Adduri et al., Cell 189 (2026), 10.1016/j.cell.2026.07.052. The State audit therefore concerns a peer-reviewed paper.

## 5. Open items (marked in red in manuscript.tex)
- corresponding e-mail, funding, confirmation of author list and contributions
- 1M-scBloodNL and Replogle/Nadig data sources (take from the download notebooks)
- DOIs to verify in references.bib (entries marked VERIFY): Zahid, Weir, OP3 author list, Nadig
- repository names and Zenodo DOI
