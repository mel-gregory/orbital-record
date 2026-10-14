# Orbital Network — Permanent Record of Its Measurements

*Live broadcast of Planet Earth. Permanent record of its measurements.*

This repository is the public archive of Orbital Network's event
store: every measurement the network's instruments took in, day by
day, exactly as the world's public agencies published it — earthquake
magnitudes and depths (USGS, EMSC), storm winds and pressures (NHC,
GDACS), wave heights, tides, water temperatures and river flows
(NOAA, USGS), natural events (NASA EONET), tsunami bulletins (NWS),
outbreak reports (WHO), and satellite element sets (CelesTrak) — each
with when it happened, when it was published, and when it reached the
record, plus the network's own cross-checks between independent
accounts of the same event.

## Layout

- `days/YYYY-MM-DD/record.json.gz` — the day's slice, verbatim from
  the store's `/record.json` export (JSON; tables keyed by name).
- `days/YYYY-MM-DD/manifest.json` — row counts, quarantine summary,
  and SHA-256 hashes for that day.
- `MANIFEST.json` — the index of all archived days and their hashes.
- `SHA256SUMS` — hashes of every archived file.

## Verify

```
sha256sum -c SHA256SUMS
```

Any file that fails its hash is not the record as exported.

## Boundaries, stated plainly

- Days are UTC, keyed on when the store took each row in. Events are
  upserts: a later day's slice re-states an event as republished, so
  the slices together form the version history.
- Quarantined records (rejected at ingest for a missing timestamp,
  bad coordinates, and the like) are counted with their sources,
  reasons, and times; their raw payloads are withheld by the store's
  standing rule and are not in this archive.
- The record begins 2026-10-13, the day the store was born. Nothing
  before that day is claimed.

The live system: https://godsky.net — the record's method is
described in *The Layers as Agents* and the founding paper,
DOI 10.5281/zenodo.23328433.
