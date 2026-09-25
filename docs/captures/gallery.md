# Capture gallery and evidence limits

## Behavior

The public gallery presents two unchanged PNG captures of the Roco Kingdom guide. Each card identifies the viewport, production source revision, and image SHA-256. The page links back to the guide and distinguishes an emulated mobile viewport from a physical-device capture.

## Provenance

Both images were captured from production version 1, deployment `appgdep_6ab5de65b7d48191a9c98e2202637567`, source revision `ecfc27f8ca5182465df891a0f516278f9af9fb7f`. Their PNG text-metadata chunk scan was empty. Validated date and time were not recorded, so the gallery labels them unavailable rather than deriving them from filenames or file timestamps.

The desktop viewport was 1440 × 1000 CSS pixels at scale 1. The portrait mobile viewport was 390 × 844 at scale 1 with touch emulation enabled. The latter is not physical-device evidence.

## Review results

The page target proof found exactly one page at the expected public URL before the interaction and capture phases. At both viewports the document accessibility root was present; there were 33 named interactive controls on desktop and 21 on emulated mobile, with no unnamed interactive controls. Tab reached the named “Skip to guide” link, whose visible focus outline measured 3 CSS pixels. The document had no horizontal overflow or out-of-bounds visible elements. The reviewed navigation requests stayed on the guide's origin, and no resource failures, HTTP statuses of 400 or greater, console errors, warnings, or unhandled exceptions were observed.

These focused checks do not certify every keyboard flow, screen reader, setting, language mode, or physical device. See the [design note](../../design/gallery-spec.md).

## Failure modes and security

A capture without a sole-target proof, exact deployment provenance, readable pixels, a checked digest, or a reviewed privacy surface is excluded. Capture-time data unavailable at capture remains unavailable. Do not publish local paths, debugger endpoints, process identifiers, profiles, or raw diagnostic files. Do not retouch, crop, reconstruct, or replace an original image.

## Verification

The preserved version-1 audit receipts validate each image's signature, dimensions, digest, viewport, target proofs, and internal field consistency. Raw receipts and captures are retained outside this source project. No test suite was run.
