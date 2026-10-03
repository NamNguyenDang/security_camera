# Implementation Source Tree

## Purpose

Mirrors the system-design component hierarchy for implementation artifacts.

Each component keeps its public API, configuration, private implementation, tests, and security material together under one ownership boundary.

## Dependency rule

Components may depend on another component's approved `api/` contract. They should not depend directly on another component's private `src/` implementation.

## Changelog

- 2026-10-03: Initial implementation scaffold created.
