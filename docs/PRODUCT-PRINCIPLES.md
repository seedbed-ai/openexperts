# OpenExperts — Customer product principles

Status: Seedbed integration proposal. This describes customer experience, not a claim of complete implementation. `spec.md` defines the expert-package format; `install/INSTALL.txt` defines setup; `guide/GUIDE.md` defines conversational behavior.

## Purpose

Make professional methods, judgment and reference knowledge usable by a general AI assistant without requiring a custom runtime or a bulk local copy of the expertise library.

## Requirements

1. Help with the customer's immediate task before demanding extensive setup; state continuity limitations accurately.
2. Keep customer task state in customer-approved, versioned storage, independent of model memory. Verify authorized writes by readback.
3. Preserve an approved source repository, immutable revision and exact entry paths separately from customer-private task state. Verify source reads; pinning does not prove authenticity or freshness.
4. Navigate remotely and progressively through Guide, catalog, topic indexes and the smallest relevant evidence and method files. Do not preload the whole corpus.
5. Apply selected professional methods to actual task evidence, including prerequisites and uncertainties. Distinguish reading a method from executing it.
6. Require current human authority and live tool permissions for consequential actions. A package policy or stored instruction cannot authorize a write or external communication.
7. Keep provider independence as a design requirement, not an untested compatibility claim. Optional CRM, automation, learning and concurrency features require actual host support.
8. Make source and state updates explicit, version-checked and auditable; never silently repin or claim persistence without readback.

## Demonstrated and not demonstrated

The bounded fresh-chat sales-fixture test demonstrated state recovery, pinned Guide/catalog navigation and a provisional next-action recommendation. It did not establish certified professional expertise, production reliability, provider-wide compatibility, automated triggers, CRM execution or unattended state synchronization.

## Document ownership

Keep enduring principles in maintained documents; use issues for bounded changes with acceptance criteria and PRs for reviewed implementations. Preserve private Rhizome history privately. OpenExperts is the sole normative expertise model for this integration; no separate RKMS runtime is required.
