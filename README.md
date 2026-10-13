# Enterprise Continuous Fraud & Risk ML Platform

A continuous, high-throughput machine learning platform for real-time payment fraud scoring, owning the lifecycle from tracked training with MLflow through automated CI/CD quality gates, canary rollouts, drift-triggered retraining (CT), and governed registry promotion.

## Data

Credit Card Fraud (ULB, via OpenML): 284,807 transactions, 492 fraud. Simulate delayed chargeback labels and document how.

- [Credit card fraud (OpenML #1597)](https://www.openml.org/d/1597)

Built step by step on the [Stacc MLOps roadmap](https://app.getstacc.org/learn/mlops). Each module adds one verified
milestone to this repository; the commit history is the build log.

## Milestones

| # | Module | Adds to this repo | Verified |
|---|---|---|---|
| 01 | Experiments & Reproducible Pipelines | Set up MLflow tracking, pipeline DAG orchestration, and environment pinning in a reproducible Docker container. | ☐ |
| 02 | CI/CD for ML | Automate pull request quality gates with code linting, data contract assertions, model regression tests, and immutable image tagging. | ☐ |
| 03 | Serving & Safe Release | Expose batch and real-time online inference with Pydantic schema validation, canary traffic routing, and automated rollback execution. | ☐ |
| 04 | Monitoring & Incident Response | Build a 4-layer telemetry system (service, data, model, business) observing drift under delayed chargeback labels and runbook execution. | ☐ |
| 05 | End-to-End ML Platform Product | Release the complete continuous ML platform with drift-triggered retraining (CT), MLflow Model Registry promotion, Terraform IaC, and SLOs. | ☐ |

Tick a row when Stacc verifies the milestone. Replace this section's intro, but keep the table:
the first milestone checks that the plan is here.

<!--
Final demo question (answer it in the capstone walkthrough):
A new model passes offline evaluation but causes an online latency spike and false-positive fraud cluster—demonstrate how the platform detects, rolls back, triggers retraining, and safely recovers.

The capstone requires a "## Walkthrough" section in this README linking a
walkthrough of five minutes or less, and CI passing on the submitted commit.
-->
