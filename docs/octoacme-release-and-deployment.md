# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Roles & Responsibilities
The following roles are accountable during the release process. See [Roles & Personas](octoacme-roles-and-personas.md) for full role descriptions and the RACI hand-off summary.

| Role | Release Responsibility |
|---|---|
| Release Manager | Owns the release schedule; facilitates go/no-go; communicates deployment plan and rollback strategy |
| PM | Confirms project milestones are met; escalates schedule conflicts |
| PdM | Signs off on release scope and release notes |
| QA Lead | Provides quality sign-off; confirms all quality gates are passed |
| DevOps Engineer | Executes or monitors the deployment pipeline; supports rollback if needed |
| Developers | Confirm all required PRs are merged; support post-deploy issue triage |

### Release Roles Checklist
- [ ] Release Manager identified and confirmed for this release
- [ ] PM has confirmed milestone alignment and approved release date
- [ ] PdM has reviewed and approved release notes
- [ ] QA Lead has provided quality sign-off (all gates passed)
- [ ] DevOps Engineer briefed on deployment window and rollback plan
- [ ] On-call rotation confirmed for post-deploy monitoring period

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback / mitigation plan documented
- Smoke tests prepared

## Deployment Checklist
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Announce release to stakeholders and support

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
