# Corio ECG

Physician-maintained research software connecting paper ECG images with digital
signals, interval measurements, quality checks, and structured reports.

This is a research prototype. It is not a validated medical device and is not
intended for clinical decision-making. Model outputs, measured intervals, and
generated reports require independent verification.

## What the code provides

- Integration with separately obtained ECG digitization and classification tools.
- Heart-rate and PR/QRS/QT/QTc measurements and rule-based rhythm analysis.
- Lead-layout, signal-quality, and diagnostic-consistency checks.
- Evaluation tools for digitization robustness, regression comparisons, and
  signal-based research.
- A local Gradio interface and structured PDF reports.
- Optional language-model narratives grounded in the structured report.

The public repository retains 158 historical commits from the maintained Corio
ECG project, with their original dates and messages. Research outputs and private
notes were filtered out of every historical tree; owner email addresses were
replaced with the maintainer's GitHub noreply address. See `HISTORY.md` for details.
It does not include patient-level evaluation results, clinical photographs,
datasets, or model weights, and does not claim established community adoption
or clinical validation.

## Setup

Use Python 3.12 in an isolated environment. The dependencies are listed in
`pyproject.toml`; `requirements.lock` records a development environment snapshot.

```bash
python3.12 -m venv .venv
source .venv/bin/activate
python -m pip install -e '.[web,dev]'
cp .env.example .env
```

Optional external components and model files are obtained separately:

```bash
python scripts/download_models.py
python scripts/setup_phase2.py
```

Review `THIRD_PARTY_NOTICES.md` and upstream requirements before downloading.
The Phase 2 setup script clones the pinned upstream repositories and downloads
model weights; the repositories and weights are not bundled here.

## Local use and tests

```bash
python -m src.web.app
python -m pytest tests
```

Tests requiring separately obtained datasets, model weights, or external tools
may be skipped or need those resources. A successful software test run does not
establish clinical performance. Evaluation scripts write outputs to `results/`;
keep per-record results private unless their redistribution is expressly allowed.

## Contributions

Bug reports, reproducible synthetic examples, tests, and documentation improvements
are welcome. See `CONTRIBUTING.md`. Do not upload patient information, identifiable
ECG images, restricted datasets, API credentials, or private logs to issues or PRs.

## Licensing

Original Corio ECG code is offered under MIT. Third-party exceptions are listed
in `THIRD_PARTY_NOTICES.md`, including the CC BY-SA 4.0 Open-ECG-Digitizer patch.
Upstream models and datasets retain their own terms.
