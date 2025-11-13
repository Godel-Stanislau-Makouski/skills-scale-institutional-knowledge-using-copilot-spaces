# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- QA Lead sign-off on test completion
- Release notes drafted
- Rollback / mitigation plan documented by DevOps Engineer
- Smoke tests prepared and reviewed

## Deployment Checklist
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests (coordinated by DevOps Engineer)
- [ ] QA Lead validates staging deployment
- [ ] Deploy to production (automated pipeline preferred, managed by DevOps Engineer)
- [ ] Run post-deploy verifications
- [ ] Announce release to stakeholders and support

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call (DevOps Engineer coordinates)
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items
  - QA Lead validates rollback or fix before re-deployment

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
