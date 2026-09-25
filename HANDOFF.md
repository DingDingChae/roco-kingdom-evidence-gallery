# Handoff

## Objective

Publish a separate public evidence gallery for reviewed captures of the Roco Kingdom guide.

## Implemented locally

- Extended the existing two-card layout to four cards, adding the reviewed 320×568 and 390×844 PNGs byte-for-byte with explicit local-static-build captions.
- Updated the public page, provenance JSON, README, capture documentation, and design handoff. New public records omit local paths and the local-only source revision.
- The 390×844 capture time is validated as 2026-09-25 06:00:25.889 UTC. The 320×568 capture date is validated as 2026-09-25 UTC; its time is unavailable.
- The two original captures remain production version 1 evidence with timestamps unavailable.
- The universal per-surface interface contract remains unverified. No redesign or new capture was performed.
- Source revision `9cac9f7990934a83b84b6b7ea0dc2d7c8d7a18fc` is on public `main`, verified with `git ls-remote`.
- Hosted publication is blocked. Saving a Sites version for the exact pushed SHA returned `repository_branch_not_found`, despite the gallery source `main` ref existing. The existing project response does not expose its configured source repository or branch when no source credential is present, so the mismatch cannot be resolved from verified fields.
- The existing Sites project remains `custom` with one allowed user, zero groups, zero external visitors, no live URL, and no saved versions. Its access was not changed. No version was saved or deployed.

## Evidence

- Baseline: production version 1, deployment `appgdep_6ab5de65b7d48191a9c98e2202637567`, source revision `ecfc27f8ca5182465df891a0f516278f9af9fb7f`.
- Desktop capture SHA-256: `eeac3abd2789431cc9953d4bc077355e73a45ced0a38f664ccd9c31ec00163ec`.
- Emulated mobile capture SHA-256: `dcb588963b29538eb02133b12921ce8f107773a68895656708fd2bd7916e92d9`.
- Both version-1 capture audit receipts validate. No test suite was run.
- Capture date and time are unavailable; no file timestamp is substituted.
- New local-build images: `roco-atlas-320x568-local-build.png` is 320×568 and `roco-atlas-390x844-local-build.png` is 390×844. Their image digests are recorded in `dist/provenance.json`; the source-only revision is intentionally excluded from public copy.
- New evidence is from checked-in static output and is not proven to represent a production deployment. Keyboard navigation was not exercised.

## Remaining

- Resolve the existing Sites source binding without changing the private guide repository or creating an unapproved credential, then save and deploy gallery edition 2 through an eligible public project.
- Verify anonymous page access and each of the four image requests separately after publication.
- The gallery remains unpublished until live page and all four image responses are verified. The broader UI contract remains incomplete even after publication.
