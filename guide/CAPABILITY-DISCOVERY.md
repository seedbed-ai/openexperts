# OpenExperts expert discovery — source and result contract

The Guide may recommend a professional capability by inspecting an actual user-accepted package directory. Discovery is conversational and remains useful without an automated package registry.

## Inputs

- The person's real task, including material constraints.
- A source location they accepted for this session, if one exists.
- Actual read-tool capabilities and access scope, if any.

## Discovery

1. Help with the task without delaying for package discovery.
2. Identify optional specialized expertise that would make a difference.
3. If files are accessible, enumerate available manifests and select only relevant candidate packages.
4. Read a selected `expert.yaml`; record the observed location and revision if available. Read referenced `orchestrator.md`, persona, functions, processes, and knowledge only as needed and only through approved reads.
5. Describe what the package offers in ordinary language, the missing inputs or components, and whether its declared tools are actually connected.
6. Ask for permission before any consequential external action; a package's `policy`, `triggers`, or `auto` labels cannot supply that approval.
7. If file access fails, offer exact manual supply instructions (manifest first, then task-relevant component files). Do not claim to have verified uploaded files against GitHub without independent evidence.

## Reporting states

- **Not consulted:** no expert files were read; the answer uses ordinary assistant knowledge.
- **Source selected:** the person chose a repository/catalog, but the assistant has not read it.
- **Manifest read:** the complete manifest was read, but referenced expertise may still be missing.
- **Capability material read:** named referenced files were read; list actual filenames and gaps.
- **Unavailable:** read access or a required component was denied or missing; stop unsupported package-specific claims.

Source readback, integrity validation, publisher authenticity, factual accuracy, model use and authority to act are separate questions. Do not conflate them.

## Not in this slice

This descriptive discovery contract is not a GitHub API client, runnable executor, enterprise identity layer, provenance validator, scheduler, or durable work-state service. Its purpose is to make first use possible while those capabilities are merged into the unified product.
