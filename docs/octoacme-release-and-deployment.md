# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Key Roles in Release Process
- **Release Manager**: Coordinates release activities, manages deployment checklist, and leads incident response
- **DevOps Engineer**: Implements and maintains CI/CD pipelines, manages infrastructure, and supports deployments
- **QA Engineer**: Validates release readiness through testing and signs off on quality gates
- **Project Manager**: Ensures stakeholder communication and tracks release dependencies
- **Developers**: Prepare code, release notes, and support deployment activities

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans (validated by DevOps Engineer)
- QA sign-off on testing and quality gates
- Release notes drafted (coordinated by Release Manager)
- Rollback / mitigation plan documented
- Smoke tests prepared and validated

## Deployment Checklist
- [ ] Deployment window scheduled (Release Manager coordinates with stakeholders)
- [ ] Backup or snapshot (DevOps Engineer prepares if applicable)
- [ ] Deploy to staging and run smoke tests (QA Engineer validates)
- [ ] Deploy to production (automated pipeline preferred, managed by DevOps Engineer)
- [ ] Run post-deploy verifications (coordinated by Release Manager)
- [ ] Announce release to stakeholders and support (Release Manager communicates)

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Release Manager triggers incident response and notifies on-call
  - DevOps Engineer executes rollback to last known-good release if necessary
  - Developers and QA triage root cause and capture action items
  - Project Manager communicates status to stakeholders

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
