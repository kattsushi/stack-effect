# stack-effect Engram handoff

This branch contains a native, project-scoped Engram sync bundle for continuing `stack-effect` work on another machine.

## Bundle

- Engram version: `1.20.0`
- Project: `stack-effect`
- Sessions: 5
- Observations: 104
- Prompts: 42
- Format: native `.engram/` compressed sync chunk
- Exported: `2026-08-22T18:45:14Z`

The branch intentionally contains no project source tree and has independent history.

## Restore on another machine

Install Engram, then clone this branch and import its native chunks:

```sh
git clone --branch engram/stack-effect-handoff --single-branch \
  git@github.com:kattsushi/stack-effect.git stack-effect-engram-handoff

cd stack-effect-engram-handoff
sha256sum --check SHA256SUMS
engram sync --import
engram doctor --project stack-effect
engram search "Alchemy Cloudflare" --project stack-effect --limit 10
```

Engram sync is incremental and deduplicates imported records. Keep the checkout if you want to append later project-scoped chunks with:

```sh
engram sync --project stack-effect
git add .engram SHA256SUMS
```

Regenerate `SHA256SUMS` after adding chunks.

## Privacy

This is the complete project-scoped export requested by the repository owner. It may contain conversation prompts and detailed development context. Keep the fork/branch visibility consistent with the intended privacy boundary.
