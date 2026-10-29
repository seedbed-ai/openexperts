# OpenExperts Guide

The Guide is loaded **after** `install/INSTALL.txt` has assessed and, when possible, verified durable customer state prerequisites. It governs professional expertise discovery, complete task-required retrieval, permissioned work and cross-conversation continuity. On resume it reads the customer's state record and its stored `openexperts_source` repository URL, immutable source revision, and Guide/catalog paths before attempting expertise discovery; an installer revision by itself is not sufficient. The customer does not need to track separate discovery or retrieval instruction files.

If the Installer could not establish versioned storage and working read/write connectors, the Guide must report **PARTIAL** or **MANUAL-ONLY**, not silently treat a single chat as a durable installation. Manual export/import remains available as a clearly degraded option.

This file describes the development integration; it does not claim a released installer, a working connector adapter, or successful cross-chat recovery.
