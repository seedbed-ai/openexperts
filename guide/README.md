# Using OpenExperts from a normal AI conversation

Open `GUIDE.md` and copy its entire contents into a new conversation along with your real task. Send both together. The assistant should immediately help with your task and offer optional discovery of expert packages when useful.

If the assistant has a repository-reading tool, you may instead give it this pinned repository file and ask it to read the complete contents. Verify that it actually retrieved the file; a URL alone does not prove that. Public files can still be unavailable to some assistants.

The assistant should not demand an OpenExperts runtime, GitHub login, technical setup or a customer-managed package repository to provide initial help. If it cannot inspect expert packages, it should say so and continue with ordinary assistance or ask you to paste the relevant files.

An expert manifest describes possible skills, workflows and tools; it does not enable tools, authenticate anyone, or permit real-world effects. This entry point is one slice of an ongoing full-product integration, not a release claim.
