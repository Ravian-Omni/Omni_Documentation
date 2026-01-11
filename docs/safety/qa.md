
# Validation & QA System

Ravian AI includes a built‑in **validation and quality assurance (QA) layer** that checks its own work and reduces the risk of silent failures.

Instead of executing a plan blindly, Ravian evaluates intermediate results and adjusts its actions when outputs look wrong or incomplete.

---

## Why validation is needed

Complex workflows can fail for many reasons:

- Unreliable web pages or APIs.
- Inconsistent data formats and missing values.
- Ambiguous instructions or edge cases the model did not anticipate.

Without validation, an agent might quietly produce low‑quality results or stop early without telling you.

Ravian’s QA system helps catch these issues and either self‑corrects or asks for guidance.

---

## What Ravian validates

During execution, Ravian performs checks such as:

- **Input/output sanity** – verifying that returned data matches expected shapes, types, or ranges.
- **Task completeness** – confirming that required sections, files, or steps are present before marking a task as done.
- **Consistency checks** – comparing multiple sources or passes to detect contradictions or gaps.
- **Guardrail checks** – ensuring actions stay within allowed scopes and policies.

!!! note
    Validation is configurable: you can tighten checks for critical workflows or relax them for quick exploratory tasks.

---

## Self‑correction loop

When a check fails, Ravian can:

1. Log the failure and reason.
2. Attempt a **self‑correction**, such as retrying a request, switching sources, or adjusting a query.
3. If repeated attempts fail, surface a clear error and suggested next steps instead of silently proceeding.
This loop reduces manual babysitting and makes failures easier to debug.

---

## Example: Validating a data report

1. You ask Ravian to create a revenue trends report from a CSV and generate a deck for leadership.
2. After loading the data, Ravian checks for missing or anomalous values and flags any severe issues.
3. It validates that all requested time periods and segments are present in the final charts and tables before finalizing the deck.
4. If a segment is missing or inconsistent, Ravian retries the query or asks you whether to exclude that segment with a clear note in the report.

The same QA principles apply to research summaries, web automations, and email workflows, increasing trust in Ravian’s autonomous execution.