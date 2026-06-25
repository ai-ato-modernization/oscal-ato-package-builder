# OSCAL ATO Package Builder

[![License: Apache-2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
[![Project Status](https://img.shields.io/badge/status-planning%20and%20prototype-lightgrey.svg)](#project-status)
[![OSCAL](https://img.shields.io/badge/OSCAL-ready-informational.svg)](#oscal-alignment)
[![ATO](https://img.shields.io/badge/ATO-package%20builder-informational.svg)](#purpose)
[![Security Policy](https://img.shields.io/badge/security-policy-brightgreen.svg)](SECURITY.md)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](#contributing)
[![Issues](https://img.shields.io/github/issues/ai-ato-modernization/oscal-ato-package-builder)](https://github.com/ai-ato-modernization/oscal-ato-package-builder/issues)
[![Pull Requests](https://img.shields.io/github/issues-pr/ai-ato-modernization/oscal-ato-package-builder)](https://github.com/ai-ato-modernization/oscal-ato-package-builder/pulls)
[![Last Commit](https://img.shields.io/github/last-commit/ai-ato-modernization/oscal-ato-package-builder)](https://github.com/ai-ato-modernization/oscal-ato-package-builder/commits/main)

## Overview

The OSCAL ATO Package Builder is an open-source reference implementation for generating Authorization to Operate package artifacts from structured evidence.

The project helps turn system information, assessment evidence, control findings, risk notes, and remediation data into consistent, reviewable, and OSCAL-ready authorization artifacts.

This repository is part of the broader `ai-ato-modernization` organization and supports the Phase-II effort to modernize ATO preparation, evidence management, control assessment, and ongoing authorization.

## Purpose

The purpose of this repository is to provide a practical way to build ATO package artifacts from structured inputs.

The project focuses on producing artifacts that are:

- Machine-readable
- Human-reviewable
- Traceable to source evidence
- Consistent across systems
- Easier to validate
- Easier to update over time
- Suitable for initial authorization and continuous monitoring workflows

This repository does not make authorization decisions. It prepares structured artifacts that system owners, assessors, risk teams, and Authorizing Officials can review.

## Scope

This repository covers:

- System Security Plan generation
- Security Assessment Plan generation
- Security Assessment Results generation
- POA&M generation
- Authorization summary generation
- Evidence-to-artifact traceability
- OSCAL-ready output structures
- Required field validation
- Sample ATO packages for different system types
- Example input and output schemas
- Validation scripts
- Reusable package templates

## Phase-II Alignment

This repository primarily supports:

### Workstream 1: Initial Authorization

It helps accelerate preparation of ATO package artifacts by converting structured system and evidence data into reviewable authorization documents.

Supported activities include:

- Creating draft authorization artifacts
- Organizing control implementation details
- Linking evidence to controls
- Preparing assessment results
- Generating POA&M entries
- Creating an authorization summary for review

### Workstream 2: Continuous Monitoring and Ongoing Authorization

The same artifact structure can be refreshed over time using updated evidence from the continuous monitoring pipeline.

Supported activities include:

- Updating assessment results
- Refreshing control evidence
- Tracking POA&M changes
- Capturing evidence freshness
- Supporting ongoing authorization review

### Workstream 3: Independent Audit Support

The generated package can support audit requests by preserving evidence traceability and producing structured summaries.

Supported activities include:

- Responding to evidence requests
- Packaging control-level artifacts
- Showing source evidence links
- Producing reviewable summaries

## Expected Deliverables

This repository is expected to produce the following deliverables:

- Sample OSCAL System Security Plan
- Sample Security Assessment Plan
- Sample Security Assessment Results
- Sample POA&M
- Sample authorization summary
- Input evidence schema
- Output artifact schema
- Validation scripts
- Example ATO package bundle
- Field mapping guide
- Evidence traceability model
- Sample packages for FISMA Low, FISMA Moderate, and cloud service provider scenarios

## Repository Structure

Recommended structure:

```text
/src
  /builder
  /validators
  /templates
  /renderers

/examples
  /fisma-low
  /fisma-moderate
  /cloud-service-provider

/oscal
  /ssp
  /sap
  /sar
  /poam

/schemas
  input-evidence.schema.json
  system-profile.schema.json
  control-implementation.schema.json
  assessment-results.schema.json
  poam.schema.json

/tests
  /fixtures
  /validation
  /golden-files

/docs
  getting-started.md
  data-model.md
  evidence-traceability.md
  oscal-alignment.md
  package-generation-flow.md
  validation-rules.md

README.md
LICENSE
CONTRIBUTING.md
SECURITY.md
ROADMAP.md
