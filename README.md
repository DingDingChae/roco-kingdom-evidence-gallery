# Roco Kingdom Guide Capture Gallery

This public project preserves two genuine captures of the public [Roco Kingdom: World Atlas & Dex](https://roco-kingdom-world-field-atlas.dewlook123.chatgpt.site/) guide. The gallery records each viewport, the verified production revision, and a SHA-256 for the unchanged PNG.

## Captures

- [Desktop overview, 1440 × 1000](dist/images/roco-atlas-desktop-1440x1000.png), image SHA-256 `eeac3abd2789431cc9953d4bc077355e73a45ced0a38f664ccd9c31ec00163ec`.
- [Portrait mobile emulation, 390 × 844](dist/images/roco-atlas-emulated-mobile-390x844.png), image SHA-256 `dcb588963b29538eb02133b12921ce8f107773a68895656708fd2bd7916e92d9`.

Both captures show production version 1 from source revision `ecfc27f8ca5182465df891a0f516278f9af9fb7f`, deployment `appgdep_6ab5de65b7d48191a9c98e2202637567`. The mobile image is emulated and does not claim physical-device evidence. Capture date and time are unavailable because the capture operation did not record a validated timestamp.

The isolated runtime review found no console errors or exceptions, requests to other origins, failed resources, unnamed interactive controls, or horizontal page overflow in either viewport. The document accessibility root was present, and Tab reached a named skip link with visible focus. These are focused checks, not a complete accessibility certification. See [the capture article](docs/captures/gallery.md) and [the design note](design/gallery-spec.md).

## License and scope

The page captures are original browser output of the referenced guide. They include no game artwork, third-party map tiles, private user data, or credentials. See [LICENSE](LICENSE) for this project's source and evidence terms.
