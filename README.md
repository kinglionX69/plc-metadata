# Proud Lions Club — metadata & images

Restored, canonical metadata and artwork for the original **Proud Lions Club (PLC)** ERC-721
collection on Ethereum mainnet.

| | |
|---|---|
| Contract | [`0xA83B409bE1Ad79EF27d8e14a3d6aAeD7B40959Dc`](https://etherscan.io/token/0xA83B409bE1Ad79EF27d8e14a3d6aAeD7B40959Dc) |
| Standard | ERC-721 (OpenZeppelin 3.1, Solidity 0.7.1) |
| Minted supply | 2,013 |
| Token ID range | 1–1920 and 7564–7977 (non-contiguous) |
| Base URI | `https://kinglionx69.github.io/plc-metadata/meta/` |
| Token URI | `<baseURI><tokenId>.json` |

## Layout

- `meta/<id>.json` — one metadata document per minted token (2,013 files)
- `images/<id>.webp` — artwork, 1080×1080, WebP quality 90 (2,013 files)

## Provenance

Artwork is the "reveal 2.0" master set, byte-identical to the original IPFS directory
`Qmbc9geseQBpwe8uX2tRHczrbWAchd21tqrtakjPNygqag`, which every metadata file still records
in its `original_image_ipfs` field. The WebP files here are re-encoded from those exact PNGs
(alpha channels were fully opaque and were dropped).

Traits come from the final "Latest Custom API Metadata" master, which carries the full
12-trait schema including Staking Power, Breeding Counter and Sex. Twelve tokens that were
left as placeholders in that master (35, 36, 38, 135, 145, 237, 889, 890, 1004, 7592, 7593,
7649) were restored from the reveal 2.0 master, which holds their real traits.

Token names and image paths were normalised so that `meta/<id>.json` always describes token
`<id>` — a handful of records in the source masters carried a mismatched `name` field.
