# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability. The Release Manager coordinates and oversees this process.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- QA Lead sign-off on test completion and quality gates
- Release notes drafted by Release Manager
- Rollback / mitigation plan documented
- Smoke tests prepared
- Support/Customer Advocate notified for customer communication planning

## Deployment Checklist
- [ ] Release Manager schedules deployment window (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] QA Lead verifies smoke test results
- [ ] Technical Architect reviews deployment plan for high-risk releases
- [ ] Release Manager deploys to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Release Manager announces release to stakeholders
- [ ] Support/Customer Advocate announces to customers and support team

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Release Manager triggers incident response and notifies on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items
  - Support/Customer Advocate communicates status to affected customers

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
