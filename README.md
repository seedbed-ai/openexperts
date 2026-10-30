# OpenExperts

OpenExperts is a file-based approach to giving an AI assistant access to professional reference material and reusable decision procedures. The current integration supports two distinct activities: navigating published expertise and maintaining customer-owned task state across conversations.

**Release-candidate status:** The Seedbed-controlled core has passed the targeted MIT source-rights review; the repository is not yet an advertised v1 release. The supported evidence is limited to a GitHub-backed, authorized task-state workflow and reviewed source navigation, not an independently verified universal runtime. See [provenance](docs/UPSTREAM-LICENSING.md).

## Start with a task

Read [Installer](install/INSTALL.txt) for setup and [Guide](guide/GUIDE.md) for task continuation. The Installer identifies a customer-approved versioned state location, requests permission before writing, and verifies saved content through an independent read. The Guide retrieves the recorded source repository and immutable revision, then consults [the catalog](CATALOG.md) to find only the relevant guidance.

The source of published methods and the customer's task record are separate. Neither setup nor a published file grants access to external accounts.

## Explore a professional example

The [fictional purchasing-decision example](examples/b2b-decision/INDEX.md) demonstrates progressive navigation from a specialty to a topic and an applicable procedure. It contains no customer records and no inherited sales-package files.

For a fictional B2B opportunity where budget approval and economic-buyer identity are unknown, the example identifies which evidence is missing and how to structure a next contact without claiming purchasing authority or a closing date.

## Package and host interfaces

[Technical interoperability notes](spec.md) describe the proposed file layout and optional manifest conventions for expert packages. Markdown and YAML can describe a method or a potential tool integration; reading them does not implement a trigger, connect a provider, or authorize actions. Features such as automated scheduling, concurrency and learning require separately implemented host behavior.

## Supported GitHub-backed v1 evidence

In the bounded accepted customer-path test, an authorized fictional task-state update was written to a customer-controlled GitHub repository, independently read back, and recovered in a fresh conversation with a newly introduced fact intact. The stored immutable OpenExperts source locator enabled pinned Guide/catalog navigation and a qualified next action. This verifies **that tested GitHub-backed workflow**, not unassisted setup for a new customer or any other storage provider.

**Not verified:** first-time uncoached Installer setup, missing permission/refusal and concurrent-version conflicts, unavailable/missing source recovery, general provider or connector compatibility, unattended synchronization, or production reliability. A newly published source revision must not silently replace a customer's stored source pin. Each customer write still requires present authorization and independent readback.

## Scope and limitations

- The [catalog](CATALOG.md) and its indexes are navigation aids, not proof that a recommendation is correct.
- Customer-owned persistence requires actual permitted storage, version checks, and post-write readback. Otherwise the Guide must label setup partial or manual-only.
- A fresh chat must use the customer's saved immutable source locator; the latest branch is not a silent substitute.
- Professional advice depends on retrieved sections and real task evidence. The example is fictional and does not certify a professional advisor.
- External writes, email, CRM changes or transactions require present authorization and available host tools.

See [product principles](docs/PRODUCT-PRINCIPLES.md), [the Guide](guide/GUIDE.md), and [the provenance and rights-status record](docs/UPSTREAM-LICENSING.md).

## Contribution and licensing status

**Core license:** The Seedbed-controlled OpenExperts core is licensed under the [MIT License](LICENSE). Legal accepted the scoped core rights and notice basis for the independently authored README, specification, Installer, Guide, catalog, interoperability notes and fictional example in the merged remediation source set. This does **not** extend the core grant to separately distributed expertise packages, customer-owned records, or uncleared inherited upstream material and historical revisions. See [provenance and exclusions](docs/UPSTREAM-LICENSING.md). This licensing clearance does not itself authorize v1 advertising, a release tag or claims of production readiness.
