# Credit risk ML platform

Your Data Science model, run like a production system on Docker Compose: tracked training, CI gates, safe releases, rollback and monitoring while labels arrive late, built locally and then run on AWS. It continues in your Data Science repo, so the model and its production setup live together.

## Data

Your Data Science model and the same UCI credit-card data. It is one historical snapshot, so late labels and shifted data are simulated. Say so wherever you report them.

- [Default of Credit Card Clients (UCI, CC BY 4.0)](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients)

Built step by step on the [Stacc MLOps roadmap](https://app.getstacc.org/learn/mlops). Each module adds one verified
milestone to this repository; the commit history is the build log.

## Milestones

| # | Module | Adds to this repo | Verified |
|---|---|---|---|
| 01 | Tracked, Repeatable Training | Bring in your Data Science model, add serving and rollback to the design doc, track runs in MLflow and rebuild it the same way in Docker. | ☐ |
| 02 | CI/CD for ML | Add CI tests that block a release when quality, cost or speed gets worse. | ☐ |
| 03 | Serving and Safe Releases | Run a canary locally with Docker Compose, then for real on AWS Lambda with a weighted alias, and roll back when it fails. | ☐ |
| 04 | Monitoring and Incidents | Monitor service, data, model and business numbers while labels arrive late, and run an incident drill. | ☐ |
| 05 | MLOps Capstone | Release the platform with triggered retraining, approved promotion in MLflow, the champion live on AWS, service targets and a walkthrough video. | ☐ |

## Acceptance evidence

Use the guided fixture and the independent variation in each module. Fix failures, then rerun every earlier test on the same candidate commit.
The filenames below are the submission contract, not supplied solutions. Implement the tests and artifacts yourself; do not commit generated caches or personal data.

### Tracked, Repeatable Training

- `README.md`
- `docker-compose.yml`
- `src/train.py`
- `docs/data_contract.md`
- `tests/test_reproduction.py`
- `docs/design.md`

### CI/CD for ML

- `.github/workflows/ci.yml`
- `tests/test_model_regression.py`
- `docs/release_gates.md`
- `tests/test_release_gate.py`

### Serving and Safe Releases

- `app/main.py`
- `Dockerfile`
- `docs/load_test.md`
- `docs/rollback.md`
- `docker-compose.yml`
- `tests/test_serving.py`
- `.github/workflows/deploy.yml`
- `README.md`

### Monitoring and Incidents

- `docs/monitoring.md`
- `docs/incident_runbook.md`
- `tests/test_delayed_labels.py`

### MLOps Capstone

- `README.md`
- `docs/slo.md`
- `docs/promotion_policy.md`
- `docker-compose.yml`
- `tests/test_continuous_training.py`
- `docs/design.md`

Keep the assessment job named `test` in GitHub Actions. It must run the actual acceptance tests; a green empty workflow does not establish correctness.
For non-Python artifacts, add the appropriate validation/integration commands to CI and retain their outputs.
Stacc's automatic checks establish artifact structure and CI status. Use the module criteria to assess numerical correctness, design quality and independent understanding.

Tick a row when Stacc verifies the milestone. Replace this section's intro, but keep the table:
the first milestone checks that the plan is here.

<!--
Final demo question (answer it in the capstone walkthrough):
A new model passes its tests, then its speed and risk-flag rate drift before the labels arrive. Show how you spot it, roll back, evaluate later and approve a fix.

The capstone requires a "## Walkthrough" section in this README linking a
walkthrough of five minutes or less, and CI passing on the submitted commit.
-->
