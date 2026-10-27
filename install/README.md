# OpenExperts — durable conversational installation

**INSTALL.txt is the Installer, not a disposable prompt launcher.** It guides the customer through the minimum prerequisites for continuing work across conversations: an approved customer-owned state location, actual read/write connector access, versioning/concurrency safeguards, permission to write, and verified write/readback.

The Installer then loads `guide/GUIDE.md` and hands over the verified storage location, version, authorized scope and limitations. **The sequence is Installer → verified state prerequisites → Guide.** Do not inject Installer and Guide simultaneously.

An assistant can still help before setup is complete. If connectors are unavailable, the customer may carry a portable state record manually, but that is a degraded fallback, not a completed durable installation.

This integration-branch text is not a published immutable release, a tested fresh-chat bootstrap, or an executable storage adapter. Never claim a successful connection or persisted record without actual tool evidence.
