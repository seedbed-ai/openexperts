# OpenExperts — proposed technical interoperability notes

**Status:** Independently authored v1 remediation draft. This is a documentation contract for review, not a claim that a compliant runtime or released SDK exists. It replaces the inherited expressive specification while retaining descriptive path and field conventions where necessary for interoperability.

## 1. Two interfaces

**Published source interface.** An assistant may discover a specialty in `CATALOG.md`, follow a compact index, inspect a selected reference section and its associated procedure, and report precisely which files and revision were read. The [fictional example](examples/b2b-decision/INDEX.md) supplies a small navigable sample.

**Customer-state interface.** A separate customer-controlled, versioned record stores objective, verified facts, unknowns, next action, evidence pointers and an immutable `openexperts_source` locator. The locator identifies source repository URL, revision, Installer path, Guide path and catalog path. It is a pointer, never a mandate to mirror the full expertise library.

The [Installer](install/INSTALL.txt) establishes prerequisites and the [Guide](guide/GUIDE.md) describes use and recovery. Their explicit consent and independent-readback requirements remain authoritative for the conversational path.

## 2. Optional package layout

Package authors and host integrators may exchange a directory with these conventional paths:

| Path | Intended role |
| --- | --- |
| `README.md` | Human-readable package orientation |
| `expert.yaml` | Descriptive package index |
| `orchestrator.md` | Starting guidance for navigating and applying a package |
| `persona/*.md` | Optional role-specific constraints |
| `functions/*.md` | Bounded procedures or decision functions |
| `processes/*.md` | Optional multi-step procedures |
| `knowledge/*.md` | Optional reference material and topic indexes |
| `tools/*.yaml` | Optional descriptions of external operations |
| `state/*.md` | Optional package examples; not an automatically writable customer store |
| `learnings/*.md`, `scratch/*.md` | Optional host-managed records |

These names aid existing integrators; this draft does not require all directories for the conversational Installer/Guide workflow. A host must validate any actual package format it elects to support.

## 3. Manifest data

An optional `expert.yaml` may carry descriptive strings `spec`, `name`, `version`, `description`, `author`, `license` and a `components` map. A declared `license` is metadata, not independent legal verification. `requires.tools` may list abstract tool names; `outputs` may list proposed deliverables.

A host that supports additional fields such as `triggers`, `concurrency`, `execution`, `delivery`, `learning` or `policy` must document its own parser and enforcement semantics. Files do not execute by themselves. A package author's `auto`, `confirm` or `manual` declaration cannot override actual account permissions, host policy or user consent.

## 4. Progressive reference selection

1. Determine what the customer is asking and what relevant evidence is missing.
2. Read the catalog at the verified pinned source revision.
3. Follow one relevant topic index instead of downloading the full corpus.
4. Fetch a small, identified reference section and the relevant method or procedure when a recommendation requires one.
5. Check prerequisite facts against customer-provided evidence. Mark unknowns and distinguish source assertions from observations.
6. Report the source repository, immutable revision, paths, selected headings and any limitations.

Index metadata alone is insufficient evidence for a domain claim. Missing or stale links must be reported, not guessed.

## 5. State creation and restart

Before any write, confirm current customer authorization, repository/storage scope, version history and conflict handling. Create or update only the approved task record. A successful write request is not proof of persistence: independently fetch the resulting state and verify its actual version and content. Do not overwrite an unrecognized newer state.

On restarting, retrieve the authorized customer record, follow its pinned `openexperts_source` locator, and load the specified Guide and catalog from that same revision. If the locator or source cannot be accessed, disclose the limitation and request a bounded repair with permission. Do not use model memory as an unannounced replacement.

## 6. Execution boundary

A host may optionally map procedure files to tools, event subscriptions, retries, approvals or learning storage. These are runtime responsibilities, not capabilities delivered by Markdown. Each consequential action requires the host's own permission checks and user authorization. No document in this repository authorizes CRM changes, email delivery, purchases or external transactions.

## 7. Compatibility and verification

The preserved names and fields are interoperability conventions, not a claim of complete compatibility with the inherited upstream 1.0 specification. Integrators should pin a source revision and test their chosen subset. Verification of a GitHub-backed conversational workflow says nothing definitive about other hosts or storage providers. This source set remains under Legal and Product review; no release is authorized.

## 8. Provenance

The project was informed by the publicly available [upstream OpenExperts project](https://github.com/dylanmeyford/openexperts/tree/91ebdd6444b6658d1cc509fc48ccf0a998c0d5fe). This replacement text was independently composed for the remediation branch, not copied or lightly paraphrased from the upstream specification. See [upstream provenance](docs/UPSTREAM-LICENSING.md) for historical declarations and outstanding rights questions.
