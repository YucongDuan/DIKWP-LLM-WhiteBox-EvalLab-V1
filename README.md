# DIKWP LLM WhiteBox EvalLab V1

A standalone, offline-first functional white-box evaluation prototype for large language models and LLM systems.

## Core idea

Map a tested LLM to the 25 DIKWP × DIKWP semantic transformation modules:

- D, I, K, W, P are both input and output semantic resource types.
- Each module contains six auditable processing units.
- A model capability is represented by module-unit evidence, 3-No handling, and critical-path traces rather than a single benchmark score.

The system separately evaluates handling of:

- incomplete input (No-Complete)
- inconsistent input (No-Consistent)
- imprecise input (No-Precise)

## Functional white-box, not private chain-of-thought extraction

The prototype does not require model weights, activations, or private chain-of-thought. It evaluates inspectable intermediate objects such as fact tables, ambiguity ledgers, evidence cards, rule cards, candidate purposes, risk tables, action tickets, residuals, and tool traces.

Open models may later add logits, activation probes, causal interventions, or internal hooks, but those are optional extensions.

## Quick start

Open `index.html` in a browser. No server, database, API key, or network is required.

Run the CLI:

```bash
python evaluate_trace.py examples/sample_run_trace.json --suite examples/probe_suite.json --out outputs
```

## Main modules

1. Model and Run Contract
2. 5×5 DIKWP Module Heatmap
3. 150 Processing Units
4. 3-No Evaluation Lab
5. Critical Path Trace
6. Probe Case Library
7. Black-box Benchmark Mapping
8. Evidence Ledger and Trace Integrity
9. Model Comparison
10. Judge Calibration and Bias Audit
11. Optimization Action Tickets
12. WhiteBox Evaluation Passport

## Boundary

The scores included in the browser demo are synthetic. They do not describe any named commercial model. Real evaluation requires frozen configurations, repeated runs, deterministic and human scoring, contamination controls, and domain review.
