# flaky-ci-demo

This repo is a live demo of how GitHub Actions handles failed job runs: a single-job workflow deliberately fails (a step that exits non-zero), so we can pull the failed job's log and point at the genuine error line, then re-run only the failed jobs and compare the run's conclusion before and after.

The workflow checks out the code with `actions/checkout` pinned to the exact release tag `v7.0.1` (the most recent release at the time this demo was set up), rather than a floating major ref such as `v7`.
