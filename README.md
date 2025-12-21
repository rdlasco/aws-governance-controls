# AWS Governance Controls

This repository documents how governance and access controls are designed, implemented, and reviewed in a small AWS environment.

The goal of this project is not to showcase every AWS service or every security framework. It is to demonstrate how governance decisions translate into real access boundaries, review processes, and evidence that can be inspected later.

Everything in this repository is built with the mindset of a junior GRC or ISSO role: define intent first, enforce it technically, and verify it through repeatable control activities.

## How This Repository Is Organized

This project is intentionally structured in phases.

Phase Zero focuses on governance design. It answers questions like who is responsible for what, how access should be scoped, and how reviews are expected to occur.

Phase One translates that intent into enforceable controls using AWS identity and logging capabilities.

Later phases focus on running controls, collecting evidence, and documenting findings the same way an analyst or auditor would expect to see them.

## Governance Design

The governance folder contains the foundational design artifacts for this environment.

- The Persona Matrix describes how responsibilities are separated between administrators, security oversight, compliance execution, and independent review.
- The Access Intent Mapping defines what access is intentionally allowed for each role and how often that access should be reviewed.

These documents are treated as living design references. They are not theoretical. They directly drive how access is implemented and how reviews are performed later in the project.
