# OpenExperts

OpenExperts is a file-based approach to giving an AI assistant access to professional reference material and reusable decision procedures. The current integration supports two distinct activities: navigating published expertise and maintaining customer-owned task state across conversations.

**Development status:** This repository documents a proposed v1, not an advertised release or a verified universal runtime. The original source and unresolved license evidence are described in [upstream provenance](docs/UPSTREAM-LICENSING.md).

## Start with a task

Read [Installer](install/INSTALL.txt) for setup and [Guide](guide/GUIDE.md) for task continuation. The Installer identifies a customer-approved versioned state location, requests permission before writing, and verifies saved content through an independent read. The Guide retrieves the recorded source repository and immutable revision, then consults [the catalog](CATALOG.md) to find only the relevant guidance.

The source of published methods and the customer's task record are separate. Neither setup nor a published file grants access to external accounts.

## Explore a professional example

The [fictional purchasing-decision example](examples/b2b-decision/INDEX.md) demonstrates progressive navigation from a specialty to a topic and an applicable procedure. It contains no customer records and no inherited sales-package files.

For a fictional B2B opportunity where budget approval and economic-buyer identity are unknown, the example identifies which evidence is missing and how to structure a next contact without claiming purchasing authority or a closing date.

## Package and host interfaces

[Technical interoperability notes](spec.md) describe the proposed file layout and optional manifest conventions for expert packages. Markdown and YAML can describe a method or a potential tool integration; reading them does not implement a trigger, connect a provider, or authorize actions. Features such as automated scheduling, concurrency and learning require separately implemented host behavior.

## Scope and limitations

- The [catalog](CATALOG.md) and its indexes are navigation aids, not proof that a recommendation is correct.
- Customer-owned persistence requires actual permitted storage, version checks, and post-write readback. Otherwise the Guide must label setup partial or manual-only.
- A fresh chat must use the customer's saved immutable source locator; the latest branch is not a silent substitute.
- Professional advice depends on retrieved sections and real task evidence. The example is fictional and does not certify a professional advisor.
- External writes, email, CRM changes or transactions require present authorization and available host tools.

See [product principles](docs/PRODUCT-PRINCIPLES.md), [the Guide](guide/GUIDE.md), and [the provenance and rights-status record](docs/UPSTREAM-LICENSING.md).

## Contribution and licensing status

**Core license selection:** The Founder approved the MIT License for Seedbed-controlled OpenExperts core material, subject to Legal validation of the holder/year notice and applicable contribution rights. The proposed license text is in [LICENSE](LICENSE). This draft contains independently authored core documentation, Installer, Guide, catalog, interoperability notes and fictional examples. Separately distributed expertise packages and customer-owned records are not licensed by this repository's core notice. Historical upstream content with unresolved rights is not retroactively licensed or endorsed. See [provenance and exact exclusions](docs/UPSTREAM-LICENSING.md). PR review, merge and advertised-release decisions remain separate.
