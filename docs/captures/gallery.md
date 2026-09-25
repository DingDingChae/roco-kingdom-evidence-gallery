# Capture gallery and evidence limits

## Behavior

The public gallery presents four unchanged PNG captures of the Roco Kingdom guide. Each card identifies its viewport and image SHA-256. The page distinguishes two production version 1 captures from two captures of a local static build. Emulated portrait viewports are not described as physical-device captures.

## Provenance

The desktop and 390 × 844 emulated-mobile images were captured from production version 1, deployment `appgdep_6ab5de65b7d48191a9c98e2202637567`, source revision `ecfc27f8ca5182465df891a0f516278f9af9fb7f`. Their PNG text-metadata chunk scan was empty. Validated date and time were not recorded, so the gallery labels them unavailable rather than deriving them from filenames or file timestamps.

The production desktop viewport was 1440 × 1000 CSS pixels at scale 1. The production portrait mobile viewport was 390 × 844 at scale 1 with touch emulation enabled. The latter is not physical-device evidence.

Two additional portrait captures show the local static build at 320 × 568 and 390 × 844, both at scale 1 with touch emulation enabled. They are not tied to a verified production deployment, and the source revision is not publicly linked. Their PNG digests match the provenance record, dimensions match the recorded viewports, and the PNG metadata scan found no text or EXIF chunks. The 320 × 568 capture has a validated date of 2026-09-25 UTC, while its capture time is unavailable. The 390 × 844 capture has a validated timestamp of 2026-09-25 06:00:25.889 UTC. The capture record says no personal data was visible, authentication was not required, and third-party requests were not expected. Keyboard navigation was not exercised for either local-build capture.

## Review results

For production version 1, the page target proof found exactly one page at the expected public URL before interaction and capture. At both viewports the document accessibility root was present; there were 33 named interactive controls on desktop and 21 on emulated mobile, with no unnamed interactive controls. Tab reached the named “Skip to guide” link, whose visible focus outline measured 3 CSS pixels. The document had no horizontal overflow or out-of-bounds visible elements. The reviewed navigation requests stayed on the guide's origin, and no resource failures, HTTP statuses of 400 or greater, console errors, warnings, or unhandled exceptions were observed.

The local-build measurements report no horizontal overflow, unnamed interactive controls, console errors, exceptions, failed resources, or bad status responses at either narrow viewport. The target URL is not recorded in the available provenance file, and the referenced raw target receipts are not present in the reviewed evidence folder. These captures therefore document pixels from the local static build, not a production deployment.

These focused checks do not certify every keyboard flow, screen reader, setting, language mode, or physical device. See the [design note](../../design/gallery-spec.md).

## Failure modes and security

A capture without readable pixels, a checked digest, and a reviewed privacy surface is excluded. Production claims additionally require exact deployment provenance and a sole-target proof. Capture-time data unavailable at capture remains unavailable. Do not publish local paths, debugger endpoints, process identifiers, profiles, or raw diagnostic files. Do not retouch, crop, reconstruct, or replace an original image.

## Verification

The preserved version-1 audit receipts validate each production image's signature, dimensions, digest, viewport, target proofs, and internal field consistency. The local-build image digests, PNG signatures, dimensions, source-output manifest, and layout measurements were checked against the available provenance. The raw target receipts for the local-build captures were not present in the reviewed evidence folder. No test suite was run.
