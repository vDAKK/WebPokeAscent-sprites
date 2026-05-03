# WebPokeAscent — Fusion Sprites

Pokémon Infinite Fusion sprites used by [WebPokeAscent](https://github.com/vDAKK/WebPokeAscent).

## Layout

```
{headSpeciesId}/
  {bodySpeciesId}.png        ← default fusion sprite
  {bodySpeciesId}a.png       ← variant a (alternate artist)
  {bodySpeciesId}b.png
  ...
  _self.png                  ← head-only (no body)
  _selfa.png
```

## Serving

Sprites are loaded via [jsDelivr](https://www.jsdelivr.com/) — no infra to run, free, cached worldwide:

```
https://cdn.jsdelivr.net/gh/vDAKK/WebPokeAscent-sprites@main/{head}/{body}.png
```

For a fresh push, jsDelivr caches for ~12h; you can force refresh by purging via their API or by bumping the branch tag.

## Source

Sprites originate from the [Pokémon Infinite Fusion](https://infinitefusion.fandom.com/) community CDN (`ifd-spaces.sfo2.cdn.digitaloceanspaces.com/custom/`). Re-fetch and re-import from the parent repo:

```bash
node api/scripts/sync_fusion_sprites.js
```

## License

Sprite art belongs to its respective artists (see `alts[].artist` in `finalFusions.json` of the parent repo). This repo is a redistribution mirror for community game integration.
